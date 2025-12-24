# sendpost-python-sdk.MessageApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_message_by_id**](MessageApi.md#get_message_by_id) | **GET** /account/message/{message_id} | Get Message


# **get_message_by_id**
> Message get_message_by_id(message_id)

Get Message

Retrieve detailed information about a specific message by its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.message import Message
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

# Configure API key authorization: accountAuth
configuration.api_key['accountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['accountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost-python-sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost-python-sdk.MessageApi(api_client)
    message_id = 'message_id_example' # str | The ID of the message to retrieve.

    try:
        # Get Message
        api_response = api_instance.get_message_by_id(message_id)
        print("The response of MessageApi->get_message_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MessageApi->get_message_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| The ID of the message to retrieve. | 

### Return type

[**Message**](Message.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful retrieval of the message. |  -  |
**404** | Message not found. |  -  |
**401** | Unauthorized. Invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

