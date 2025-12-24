# sendpost-python-sdk.EmailApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**send_email**](EmailApi.md#send_email) | **POST** /subaccount/email/ | Send Email
[**send_email_with_template**](EmailApi.md#send_email_with_template) | **POST** /subaccount/email/template | Send Email With Template


# **send_email**
> List[EmailResponse] send_email(email_message_object)

Send Email

Use this API to send either a single or batch email.

### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.email_message_object import EmailMessageObject
from sendpost-python-sdk.models.email_response import EmailResponse
from sendpost-python-sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost-python-sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: subAccountAuth
configuration.api_key['subAccountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subAccountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost-python-sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost-python-sdk.EmailApi(api_client)
    email_message_object = sendpost-python-sdk.EmailMessageObject() # EmailMessageObject | Email message details

    try:
        # Send Email
        api_response = api_instance.send_email(email_message_object)
        print("The response of EmailApi->send_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->send_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_message_object** | [**EmailMessageObject**](EmailMessageObject.md)| Email message details | 

### Return type

[**List[EmailResponse]**](EmailResponse.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of email message response objects. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_email_with_template**
> List[EmailResponse] send_email_with_template(email_message_with_template)

Send Email With Template

Use this API to send an email with a predefined template. This makes it easy to integrate transactional emails with minimal code.


### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.email_message_with_template import EmailMessageWithTemplate
from sendpost-python-sdk.models.email_response import EmailResponse
from sendpost-python-sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost-python-sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: subAccountAuth
configuration.api_key['subAccountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subAccountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost-python-sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost-python-sdk.EmailApi(api_client)
    email_message_with_template = sendpost-python-sdk.EmailMessageWithTemplate() # EmailMessageWithTemplate | Email message details with template information

    try:
        # Send Email With Template
        api_response = api_instance.send_email_with_template(email_message_with_template)
        print("The response of EmailApi->send_email_with_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->send_email_with_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_message_with_template** | [**EmailMessageWithTemplate**](EmailMessageWithTemplate.md)| Email message details with template information | 

### Return type

[**List[EmailResponse]**](EmailResponse.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of email message response objects. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

