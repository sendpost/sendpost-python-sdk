# SendPost Python SDK

The official Python SDK for SendPost - a powerful email API service for sending transactional and marketing emails with advanced tracking and analytics.

## Features

- Send personalized emails to multiple recipients
- Track email opens and clicks
- Monitor email statistics (bounces, unsubscribes, spam reports)
- Manage multiple sub-accounts
- Domain and sender management
- Webhook support for real-time event notifications
- IP pool management for better deliverability

## Requirements

- Python 3.9 or higher
- A SendPost account ([Sign up here](https://app.sendpost.io/register))

## Installation

### Option 1: Install from GitHub (Recommended)

Install the SDK directly from the GitHub repository:

```bash
pip install git+https://github.com/sendpost/sendpost-python-sdk.git
```

If you need to install for all users (requires admin/sudo privileges):

```bash
sudo pip install git+https://github.com/sendpost/sendpost-python-sdk.git
```

### Option 2: Install from Local Source

If you've cloned the repository locally:

```bash
cd sendpost-python-sdk
pip install .
```

Or for development mode:

```bash
pip install -e .
```

### Option 3: Using pip with requirements.txt

Add the following to your `requirements.txt`:

```
git+https://github.com/sendpost/sendpost-python-sdk.git
```

Then install:

```bash
pip install -r requirements.txt
```

### Verify Installation

To verify the SDK is installed correctly:

```python
import sendpost_python_sdk
print(sendpost_python_sdk.__version__)
```

## Quick Start

### 1. Get Your API Keys

1. Sign up for a SendPost account at [https://app.sendpost.io/register](https://app.sendpost.io/register)
2. Navigate to your dashboard to get your API keys:
   - **Sub-Account API Key** (`X-SubAccount-ApiKey`): Used for sending emails and managing domains
   - **Account API Key** (`X-Account-ApiKey`): Used for managing sub-accounts and IPs

### 2. Send Your First Email

```python
import sendpost_python_sdk
from sendpost_python_sdk import Configuration, ApiClient
from sendpost_python_sdk.api import EmailApi
from sendpost_python_sdk.models import EmailMessageObject, EmailAddress, Recipient

# Configure the SDK
configuration = Configuration(
    host="https://api.sendpost.io/api/v1"
)

# Set your Sub-Account API Key
configuration.api_key['subAccountAuth'] = 'YOUR_SUB_ACCOUNT_API_KEY'

# Create the email message
email_message = EmailMessageObject()

# Set sender
from_addr = EmailAddress()
from_addr.email = "sender@yourdomain.com"
from_addr.name = "Your Name"
email_message.var_from = from_addr

# Set recipient
recipient = Recipient()
recipient.email = "recipient@example.com"
recipient.name = "Recipient Name"
email_message.to = [recipient]

# Set email content
email_message.subject = "Hello from SendPost!"
email_message.html_body = "<h1>Welcome!</h1><p>This is your first email sent with SendPost.</p>"
email_message.text_body = "Welcome! This is your first email sent with SendPost."

# Enable tracking
email_message.track_opens = True
email_message.track_clicks = True

# Send the email
with ApiClient(configuration) as api_client:
    email_api = EmailApi(api_client)
    try:
        responses = email_api.send_email(email_message)
        if responses:
            print(f"Email sent successfully! Message ID: {responses[0].message_id}")
    except sendpost_python_sdk.exceptions.ApiException as e:
        print(f"Error sending email: {e}")
```

### 3. Using Environment Variables

For better security, store your API keys as environment variables:

```bash
export SENDPOST_SUB_ACCOUNT_API_KEY="your_sub_account_api_key"
export SENDPOST_ACCOUNT_API_KEY="your_account_api_key"
```

Then use them in your code:

```python
import os
import sendpost_python_sdk
from sendpost_python_sdk import Configuration, ApiClient

configuration = Configuration(host="https://api.sendpost.io/api/v1")
configuration.api_key['subAccountAuth'] = os.getenv('SENDPOST_SUB_ACCOUNT_API_KEY')
```

## Common Use Cases

### Send Transactional Email

```python
from sendpost_python_sdk import Configuration, ApiClient
from sendpost_python_sdk.api import EmailApi
from sendpost_python_sdk.models import EmailMessageObject, EmailAddress, Recipient

config = Configuration(host="https://api.sendpost.io/api/v1")
config.api_key['subAccountAuth'] = 'YOUR_SUB_ACCOUNT_API_KEY'

email = EmailMessageObject()
email.var_from = EmailAddress(email="noreply@yourdomain.com", name="Your App")
email.to = [Recipient(email="user@example.com", name="User")]
email.subject = "Order Confirmation"
email.html_body = "<h1>Thank you for your order!</h1>"
email.text_body = "Thank you for your order!"
email.track_opens = True
email.track_clicks = True

with ApiClient(config) as client:
    api = EmailApi(client)
    response = api.send_email(email)
    print(f"Sent: {response[0].message_id}")
```

### List Domains

```python
from sendpost_python_sdk import Configuration, ApiClient
from sendpost_python_sdk.api import DomainApi

config = Configuration(host="https://api.sendpost.io/api/v1")
config.api_key['subAccountAuth'] = 'YOUR_SUB_ACCOUNT_API_KEY'

with ApiClient(config) as client:
    domain_api = DomainApi(client)
    domains = domain_api.get_all_domains()
    for domain in domains:
        print(f"Domain: {domain.name}, Verified: {domain.verified}")
```

### Get Email Statistics

```python
from sendpost_python_sdk import Configuration, ApiClient
from sendpost_python_sdk.api import StatsApi
from datetime import date, timedelta

config = Configuration(host="https://api.sendpost.io/api/v1")
config.api_key['accountAuth'] = 'YOUR_ACCOUNT_API_KEY'

to_date = date.today()
from_date = to_date - timedelta(days=7)
subaccount_id = 123  # Your sub-account ID

with ApiClient(config) as client:
    stats_api = StatsApi(client)
    stats = stats_api.account_subaccount_stat_subaccount_id_get(
        from_date, to_date, subaccount_id
    )
    for stat in stats:
        print(f"Date: {stat.date}")
        if stat.stats:
            print(f"  Processed: {stat.stats.processed}")
            print(f"  Delivered: {stat.stats.delivered}")
            print(f"  Opens: {stat.stats.opened}")
            print(f"  Clicks: {stat.stats.clicked}")
```

### Create a Sub-Account

```python
from sendpost_python_sdk import Configuration, ApiClient
from sendpost_python_sdk.api import SubAccountApi
from sendpost_python_sdk.models import CreateSubAccountRequest

config = Configuration(host="https://api.sendpost.io/api/v1")
config.api_key['accountAuth'] = 'YOUR_ACCOUNT_API_KEY'

with ApiClient(config) as client:
    sub_account_api = SubAccountApi(client)
    request = CreateSubAccountRequest()
    request.name = "My New Sub-Account"
    sub_account = sub_account_api.create_sub_account(request)
    print(f"Created sub-account: {sub_account.name}")
    print(f"API Key: {sub_account.api_key}")
```

## Authentication

SendPost uses API keys for authentication. There are two types of API keys:

1. **Sub-Account API Key** (`X-SubAccount-ApiKey`): Used for:
   - Sending emails
   - Managing domains and senders
   - Viewing email statistics
   - Managing suppressions

2. **Account API Key** (`X-Account-ApiKey`): Used for:
   - Creating and managing sub-accounts
   - Managing IP addresses and IP pools
   - Account-level statistics
   - Managing webhooks

Set the appropriate API key based on the operation you're performing:

```python
# For sub-account operations
config.api_key['subAccountAuth'] = 'YOUR_SUB_ACCOUNT_API_KEY'

# For account operations
config.api_key['accountAuth'] = 'YOUR_ACCOUNT_API_KEY'
```

## Error Handling

The SDK raises `ApiException` for API errors. Always wrap API calls in try-except blocks:

```python
from sendpost_python_sdk.exceptions import ApiException

try:
    response = email_api.send_email(email_message)
    except ApiException as e:
    print(f"API Error: Status {e.status}")
    print(f"Reason: {e.reason}")
    print(f"Body: {e.body}")
except Exception as e:
    print(f"Unexpected error: {e}")
```

## API Reference

### Available APIs

| API Class | Description |
|-----------|-------------|
| `EmailApi` | Send emails and manage email templates |
| `DomainApi` | Add, verify, and manage sending domains |
| `SubAccountApi` | Create and manage sub-accounts |
| `StatsApi` | Retrieve email statistics and analytics |
| `MessageApi` | Get details about sent messages |
| `WebhookApi` | Create and manage webhooks for event notifications |
| `IPApi` | Manage IP addresses |
| `IPPoolsApi` | Create and manage IP pools |
| `SuppressionApi` | Manage suppression lists |

### Complete API Documentation

For detailed API documentation, see the [docs](docs/) directory or visit our [API Reference](https://docs.sendpost.io).

## Examples

Check out the [example-sdk-python](../example-sdk-python/) directory for comprehensive examples including:

- Sending transactional and marketing emails
- Domain management
- Sub-account creation
- Statistics retrieval
- Webhook setup
- IP pool management

## Testing

Run the test suite:

```bash
pytest
```

## Support

- **Documentation**: [https://docs.sendpost.io](https://docs.sendpost.io)
- **Email**: hello@sendpost.io
- **Website Chat**: Available on [https://app.sendpost.io](https://app.sendpost.io)

## License

This SDK is generated by [OpenAPI Generator](https://openapi-generator.tech).

- API version: 1.0.0
- Package version: 1.0.0
- Generator version: 7.13.0

## Additional Resources

- [SendPost Website](https://sendpost.io)
- [Developer Portal](https://app.sendpost.io)
- [Other SDKs](https://github.com/sendpost):
  - [PHP SDK](https://github.com/sendpost/sendpost_php_sdk)
  - [JavaScript SDK](https://github.com/sendpost/sendpost_javascript_sdk)
  - [Ruby SDK](https://github.com/sendpost/sendpost_ruby_sdk)
  - [Go SDK](https://github.com/sendpost/sendpost_go_sdk)
