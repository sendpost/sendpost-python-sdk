# sendpost_python_sdk.IPPoolsApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ip_pool**](IPPoolsApi.md#create_ip_pool) | **POST** /account/ippool | Create IPPool
[**delete_ip_pool**](IPPoolsApi.md#delete_ip_pool) | **DELETE** /account/ippool/{ippool_id} | Delete IPPool
[**get_all_ip_pools**](IPPoolsApi.md#get_all_ip_pools) | **GET** /account/ippool | List IPPools
[**get_ip_pool_by_id**](IPPoolsApi.md#get_ip_pool_by_id) | **GET** /account/ippool/{ippool_id} | Get IPPool
[**update_ip_pool**](IPPoolsApi.md#update_ip_pool) | **PUT** /account/ippool/{ippool_id} | Update IPPool


# **create_ip_pool**
> IPPool create_ip_pool(ip_pool_create_request)

Create IPPool

Creates a new IPPool with the specified name, IPs, and third-party sending providers.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.ip_pool import IPPool
from sendpost_python_sdk.models.ip_pool_create_request import IPPoolCreateRequest
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
    api_instance = sendpost_python_sdk.IPPoolsApi(api_client)
    ip_pool_create_request = {"name":"Marketing Promotional","tpsps":[1],"ips":[{"publicIP":"3.238.19.87"}]} # IPPoolCreateRequest | 

    try:
        # Create IPPool
        api_response = api_instance.create_ip_pool(ip_pool_create_request)
        print("The response of IPPoolsApi->create_ip_pool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPPoolsApi->create_ip_pool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ip_pool_create_request** | [**IPPoolCreateRequest**](IPPoolCreateRequest.md)|  | 

### Return type

[**IPPool**](IPPool.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Created IPPool details |  -  |
**403** | Forbidden, IPPool with the same name already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ip_pool**
> IPPoolDeleteResponse delete_ip_pool(ippool_id)

Delete IPPool

Delete a specific IPPool based on its ID.

### Example


```python
import sendpost_python_sdk
from sendpost_python_sdk.models.ip_pool_delete_response import IPPoolDeleteResponse
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
    api_instance = sendpost_python_sdk.IPPoolsApi(api_client)
    ippool_id = 756 # int | The ID of the IPPool to delete

    try:
        # Delete IPPool
        api_response = api_instance.delete_ip_pool(ippool_id)
        print("The response of IPPoolsApi->delete_ip_pool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPPoolsApi->delete_ip_pool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ippool_id** | **int**| The ID of the IPPool to delete | 

### Return type

[**IPPoolDeleteResponse**](IPPoolDeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful deletion of the IPPool |  -  |
**404** | IPPool not found |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_ip_pools**
> List[IPPool] get_all_ip_pools(limit=limit, offset=offset, search=search)

List IPPools

Retrieves a list of all IPPools and information about all IPs contained in that pool.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.ip_pool import IPPool
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
    api_instance = sendpost_python_sdk.IPPoolsApi(api_client)
    limit = 10 # int | Number of records to return per request (optional)
    offset = 0 # int | Number of initial records to skip (optional)
    search = 'Transactional' # str | Case insensitive search against IPPool name (optional)

    try:
        # List IPPools
        api_response = api_instance.get_all_ip_pools(limit=limit, offset=offset, search=search)
        print("The response of IPPoolsApi->get_all_ip_pools:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPPoolsApi->get_all_ip_pools: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of records to return per request | [optional] 
 **offset** | **int**| Number of initial records to skip | [optional] 
 **search** | **str**| Case insensitive search against IPPool name | [optional] 

### Return type

[**List[IPPool]**](IPPool.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of IPPools |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ip_pool_by_id**
> IPPool get_ip_pool_by_id(ippool_id)

Get IPPool

Retrieves details of a specific IPPool based on its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.ip_pool import IPPool
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
    api_instance = sendpost_python_sdk.IPPoolsApi(api_client)
    ippool_id = 74 # int | The ID of the IPPool whose information you want to retrieve

    try:
        # Get IPPool
        api_response = api_instance.get_ip_pool_by_id(ippool_id)
        print("The response of IPPoolsApi->get_ip_pool_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPPoolsApi->get_ip_pool_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ippool_id** | **int**| The ID of the IPPool whose information you want to retrieve | 

### Return type

[**IPPool**](IPPool.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Details of a specific IPPool |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ip_pool**
> IPPool update_ip_pool(ippool_id, ip_pool_update_request)

Update IPPool

Update the details of an existing IPPool by its ID.

### Example


```python
import sendpost_python_sdk
from sendpost_python_sdk.models.ip_pool import IPPool
from sendpost_python_sdk.models.ip_pool_update_request import IPPoolUpdateRequest
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
    api_instance = sendpost_python_sdk.IPPoolsApi(api_client)
    ippool_id = 756 # int | The ID of the IPPool to update
    ip_pool_update_request = {"name":"Marketing Promotional","ips":[{"publicIP":"52.12.10.12"},{"publicIP":"52.10.12.17"},{"publicIP":"35.11.10.5"}]} # IPPoolUpdateRequest | 

    try:
        # Update IPPool
        api_response = api_instance.update_ip_pool(ippool_id, ip_pool_update_request)
        print("The response of IPPoolsApi->update_ip_pool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPPoolsApi->update_ip_pool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ippool_id** | **int**| The ID of the IPPool to update | 
 **ip_pool_update_request** | [**IPPoolUpdateRequest**](IPPoolUpdateRequest.md)|  | 

### Return type

[**IPPool**](IPPool.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated IPPool details |  -  |
**400** | Bad request - invalid or missing data |  -  |
**404** | IPPool not found |  -  |
**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

