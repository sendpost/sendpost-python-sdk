# sendpost_python_sdk.SuppressionApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_suppression**](SuppressionApi.md#create_suppression) | **POST** /subaccount/suppression | Create Suppressions
[**delete_suppression**](SuppressionApi.md#delete_suppression) | **DELETE** /subaccount/suppression | Delete Suppressions
[**get_suppression_list**](SuppressionApi.md#get_suppression_list) | **GET** /subaccount/suppression | List Suppressions


# **create_suppression**
> List[Suppression] create_suppression(create_suppression_request)

Create Suppressions

Creates new suppressions by posting to the suppression resource. You can specify different types of suppressions including `hardBounce`, `manual`, `unsubscribe`, and `spamComplaint`.


### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.create_suppression_request import CreateSuppressionRequest
from sendpost_python_sdk.models.suppression import Suppression
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

# Configure API key authorization: subAccountAuth
configuration.api_key['subAccountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subAccountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.SuppressionApi(api_client)
    create_suppression_request = sendpost_python_sdk.CreateSuppressionRequest() # CreateSuppressionRequest | 

    try:
        # Create Suppressions
        api_response = api_instance.create_suppression(create_suppression_request)
        print("The response of SuppressionApi->create_suppression:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SuppressionApi->create_suppression: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_suppression_request** | [**CreateSuppressionRequest**](CreateSuppressionRequest.md)|  | 

### Return type

[**List[Suppression]**](Suppression.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of created suppressions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_suppression**
> List[DeleteSuppression200ResponseInner] delete_suppression(delete_suppression_request)

Delete Suppressions

Deletes one or more suppressions for a given sub-account. The request can contain a list of emails to delete specific suppressions or delete a single suppression.


### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.delete_suppression200_response_inner import DeleteSuppression200ResponseInner
from sendpost_python_sdk.models.delete_suppression_request import DeleteSuppressionRequest
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

# Configure API key authorization: subAccountAuth
configuration.api_key['subAccountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subAccountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.SuppressionApi(api_client)
    delete_suppression_request = sendpost_python_sdk.DeleteSuppressionRequest() # DeleteSuppressionRequest | 

    try:
        # Delete Suppressions
        api_response = api_instance.delete_suppression(delete_suppression_request)
        print("The response of SuppressionApi->delete_suppression:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SuppressionApi->delete_suppression: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delete_suppression_request** | [**DeleteSuppressionRequest**](DeleteSuppressionRequest.md)|  | 

### Return type

[**List[DeleteSuppression200ResponseInner]**](DeleteSuppression200ResponseInner.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A message indicating successful suppression deletion |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_suppression_list**
> List[Suppression] get_suppression_list(var_from, to, limit=limit, offset=offset, search=search, type=type)

List Suppressions

Retrieves a list of suppressions associated with a specific sub-account within a given date range.
The maximum difference between `from` and `to` dates should not exceed 60 days.


### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.suppression import Suppression
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

# Configure API key authorization: subAccountAuth
configuration.api_key['subAccountAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['subAccountAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with sendpost_python_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sendpost_python_sdk.SuppressionApi(api_client)
    var_from = '2013-10-20' # date | Start date for the suppression records
    to = '2013-10-20' # date | End date for the suppression records (Note: `from` should be earlier than `to` and the date range should not exceed 60 days) 
    limit = 20 # int | Number of records to return per request (optional) (default to 20)
    offset = 0 # int | Number of initial records to skip (optional) (default to 0)
    search = 'search_example' # str | Case-insensitive search against suppression email (optional)
    type = 'type_example' # str | Type of suppression. Valid values: `hardBounce`, `manual`, `spamComplaint`, `unsubscribe`  (optional)

    try:
        # List Suppressions
        api_response = api_instance.get_suppression_list(var_from, to, limit=limit, offset=offset, search=search, type=type)
        print("The response of SuppressionApi->get_suppression_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SuppressionApi->get_suppression_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **date**| Start date for the suppression records | 
 **to** | **date**| End date for the suppression records (Note: &#x60;from&#x60; should be earlier than &#x60;to&#x60; and the date range should not exceed 60 days)  | 
 **limit** | **int**| Number of records to return per request | [optional] [default to 20]
 **offset** | **int**| Number of initial records to skip | [optional] [default to 0]
 **search** | **str**| Case-insensitive search against suppression email | [optional] 
 **type** | **str**| Type of suppression. Valid values: &#x60;hardBounce&#x60;, &#x60;manual&#x60;, &#x60;spamComplaint&#x60;, &#x60;unsubscribe&#x60;  | [optional] 

### Return type

[**List[Suppression]**](Suppression.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of suppressions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

