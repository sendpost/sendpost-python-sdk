# sendpost-python-sdk.IPApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**allocate_new_ip**](IPApi.md#allocate_new_ip) | **PUT** /account/ip/allocate | Allocate IP
[**delete_ip**](IPApi.md#delete_ip) | **DELETE** /account/ip/{ip_id} | Delete IP
[**get_all_ips**](IPApi.md#get_all_ips) | **GET** /account/ip/ | List IPs
[**get_specific_ip**](IPApi.md#get_specific_ip) | **GET** /account/ip/{ip_id} | Get IP
[**update_ip**](IPApi.md#update_ip) | **PUT** /account/ip/{ip_id} | Update IP


# **allocate_new_ip**
> IP allocate_new_ip(ip_allocation_request)

Allocate IP

Allocates a new IP resource to the account.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.ip import IP
from sendpost-python-sdk.models.ip_allocation_request import IPAllocationRequest
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
    api_instance = sendpost-python-sdk.IPApi(api_client)
    ip_allocation_request = sendpost-python-sdk.IPAllocationRequest() # IPAllocationRequest | 

    try:
        # Allocate IP
        api_response = api_instance.allocate_new_ip(ip_allocation_request)
        print("The response of IPApi->allocate_new_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPApi->allocate_new_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ip_allocation_request** | [**IPAllocationRequest**](IPAllocationRequest.md)|  | 

### Return type

[**IP**](IP.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Details of the allocated IP |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ip**
> IPDeletionResponse delete_ip(ip_id)

Delete IP

Deletes a specific IP resource based on the provided IP ID.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.ip_deletion_response import IPDeletionResponse
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
    api_instance = sendpost-python-sdk.IPApi(api_client)
    ip_id = 56 # int | The ID of the IP resource to delete

    try:
        # Delete IP
        api_response = api_instance.delete_ip(ip_id)
        print("The response of IPApi->delete_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPApi->delete_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ip_id** | **int**| The ID of the IP resource to delete | 

### Return type

[**IPDeletionResponse**](IPDeletionResponse.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Confirmation message after successful IP deletion |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_ips**
> List[IP] get_all_ips(limit=limit, offset=offset, search=search)

List IPs

Retrieves a list of all IPs associated with the main account.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.ip import IP
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
    api_instance = sendpost-python-sdk.IPApi(api_client)
    limit = 56 # int | Number of records to return per request (optional)
    offset = 56 # int | Number of initial records to skip (optional)
    search = 'search_example' # str | Case insensitive search against IP's public IP address (optional)

    try:
        # List IPs
        api_response = api_instance.get_all_ips(limit=limit, offset=offset, search=search)
        print("The response of IPApi->get_all_ips:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPApi->get_all_ips: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of records to return per request | [optional] 
 **offset** | **int**| Number of initial records to skip | [optional] 
 **search** | **str**| Case insensitive search against IP&#39;s public IP address | [optional] 

### Return type

[**List[IP]**](IP.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of IPs associated with the account |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_specific_ip**
> IP get_specific_ip(ip_id)

Get IP

Retrieves detailed information about a specific IP based on the provided ID.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.ip import IP
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
    api_instance = sendpost-python-sdk.IPApi(api_client)
    ip_id = 56 # int | The ID of the IP resource to retrieve

    try:
        # Get IP
        api_response = api_instance.get_specific_ip(ip_id)
        print("The response of IPApi->get_specific_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPApi->get_specific_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ip_id** | **int**| The ID of the IP resource to retrieve | 

### Return type

[**IP**](IP.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Information about the specified IP |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ip**
> IP update_ip(ip_id, ip_update_request)

Update IP

Updates an existing IP resource based on the provided IP ID.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.ip import IP
from sendpost-python-sdk.models.ip_update_request import IPUpdateRequest
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
    api_instance = sendpost-python-sdk.IPApi(api_client)
    ip_id = 56 # int | The ID of the IP resource to update
    ip_update_request = sendpost-python-sdk.IPUpdateRequest() # IPUpdateRequest | 

    try:
        # Update IP
        api_response = api_instance.update_ip(ip_id, ip_update_request)
        print("The response of IPApi->update_ip:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IPApi->update_ip: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ip_id** | **int**| The ID of the IP resource to update | 
 **ip_update_request** | [**IPUpdateRequest**](IPUpdateRequest.md)|  | 

### Return type

[**IP**](IP.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated IP information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

