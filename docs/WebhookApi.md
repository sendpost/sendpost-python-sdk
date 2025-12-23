# sendpost_python_sdk.WebhookApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook**](WebhookApi.md#create_webhook) | **POST** /account/webhook | Create Webhook
[**delete_webhook**](WebhookApi.md#delete_webhook) | **DELETE** /account/webhook/{webhook_id} | Delete Webhook
[**get_all_webhooks**](WebhookApi.md#get_all_webhooks) | **GET** /account/webhook | List Webhooks
[**get_webhook**](WebhookApi.md#get_webhook) | **GET** /account/webhook/{webhook_id} | Get Webhook
[**update_webhook**](WebhookApi.md#update_webhook) | **PUT** /account/webhook/{webhook_id} | Update Webhook


# **create_webhook**
> Webhook create_webhook(create_webhook_request)

Create Webhook

Create a new webhook by specifying its properties.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.create_webhook_request import CreateWebhookRequest
from sendpost_python_sdk.models.webhook import Webhook
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookApi(api_client)
    create_webhook_request = sendpost_python_sdk.CreateWebhookRequest() # CreateWebhookRequest | 

    try:
        # Create Webhook
        api_response = api_instance.create_webhook(create_webhook_request)
        print("The response of WebhookApi->create_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhookApi->create_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_webhook_request** | [**CreateWebhookRequest**](CreateWebhookRequest.md)|  | 

### Return type

[**Webhook**](Webhook.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Webhook created successfully. |  -  |
**401** | Unauthorized. Invalid API key. |  -  |
**403** | Forbidden. Webhook with the same URL already exists. |  -  |
**406** | Not Acceptable. Cannot create webhook for the default sub-account. |  -  |
**422** | Unprocessable entity. Invalid request body. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_webhook**
> DeleteWebhookResponse delete_webhook(webhook_id)

Delete Webhook

Delete a webhook by its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.delete_webhook_response import DeleteWebhookResponse
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookApi(api_client)
    webhook_id = 117 # int | ID of the webhook to delete.

    try:
        # Delete Webhook
        api_response = api_instance.delete_webhook(webhook_id)
        print("The response of WebhookApi->delete_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhookApi->delete_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_id** | **int**| ID of the webhook to delete. | 

### Return type

[**DeleteWebhookResponse**](DeleteWebhookResponse.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_webhooks**
> List[Webhook] get_all_webhooks(limit=limit, offset=offset, search=search)

List Webhooks

Retrieves a list of all webhooks, their endpoints, and the events for which they are active.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.webhook import Webhook
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookApi(api_client)
    limit = 10 # int | Number of records to return per request. (optional)
    offset = 0 # int | Number of initial records to skip. (optional)
    search = 'hooli' # str | Case insensitive search against webhook URL. (optional)

    try:
        # List Webhooks
        api_response = api_instance.get_all_webhooks(limit=limit, offset=offset, search=search)
        print("The response of WebhookApi->get_all_webhooks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhookApi->get_all_webhooks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of records to return per request. | [optional] 
 **offset** | **int**| Number of initial records to skip. | [optional] 
 **search** | **str**| Case insensitive search against webhook URL. | [optional] 

### Return type

[**List[Webhook]**](Webhook.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of webhooks. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_webhook**
> Webhook get_webhook(webhook_id)

Get Webhook

Retrieves a specific webhook based on its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.webhook import Webhook
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookApi(api_client)
    webhook_id = 117 # int | The ID of the webhook to retrieve.

    try:
        # Get Webhook
        api_response = api_instance.get_webhook(webhook_id)
        print("The response of WebhookApi->get_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhookApi->get_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_id** | **int**| The ID of the webhook to retrieve. | 

### Return type

[**Webhook**](Webhook.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook details. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_webhook**
> Webhook update_webhook(webhook_id, update_webhook)

Update Webhook

Update the properties of an existing webhook.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.update_webhook import UpdateWebhook
from sendpost_python_sdk.models.webhook import Webhook
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookApi(api_client)
    webhook_id = 117 # int | ID of the webhook to update.
    update_webhook = sendpost_python_sdk.UpdateWebhook() # UpdateWebhook | 

    try:
        # Update Webhook
        api_response = api_instance.update_webhook(webhook_id, update_webhook)
        print("The response of WebhookApi->update_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhookApi->update_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_id** | **int**| ID of the webhook to update. | 
 **update_webhook** | [**UpdateWebhook**](UpdateWebhook.md)|  | 

### Return type

[**Webhook**](Webhook.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

