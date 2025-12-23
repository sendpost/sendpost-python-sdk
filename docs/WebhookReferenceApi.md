# sendpost_python_sdk.WebhookReferenceApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**send_post_webhooks_post**](WebhookReferenceApi.md#send_post_webhooks_post) | **POST** /SendPostWebhooks | SendPost Webhook Object


# **send_post_webhooks_post**
> send_post_webhooks_post(webhook_object=webhook_object)

SendPost Webhook Object

### Example


```python
import sendpost_python_sdk
from sendpost_python_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendpost.io/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = sendpost_python_sdk.Configuration(
    host = "https://api.sendpost.io/api/v1"
)


# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.WebhookReferenceApi(api_client)
    webhook_object = sendpost_python_sdk.WebhookObject() # WebhookObject |  (optional)

    try:
        # SendPost Webhook Object
        api_instance.send_post_webhooks_post(webhook_object=webhook_object)
    except Exception as e:
        print("Exception when calling WebhookReferenceApi->send_post_webhooks_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_object** | [**WebhookObject**](WebhookObject.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Return a 200 status to indicate that the data was received successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

