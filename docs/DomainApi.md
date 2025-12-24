# sendpost_python_sdk.DomainApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_all_domains**](DomainApi.md#get_all_domains) | **GET** /subaccount/domain | List Domains
[**subaccount_domain_domain_id_delete**](DomainApi.md#subaccount_domain_domain_id_delete) | **DELETE** /subaccount/domain/{domain_id} | Delete Domain
[**subaccount_domain_domain_id_get**](DomainApi.md#subaccount_domain_domain_id_get) | **GET** /subaccount/domain/{domain_id} | Get Domain
[**subaccount_domain_post**](DomainApi.md#subaccount_domain_post) | **POST** /subaccount/domain | Create Domain


# **get_all_domains**
> List[Domain] get_all_domains(limit=limit, offset=offset, search=search)

List Domains

Retrieve a list of all domains associated with the sub-account, including their DNS records and authentication status.


### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.domain import Domain
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
    api_instance = sendpost_python_sdk.DomainApi(api_client)
    limit = 56 # int | Number of records to return per request (optional)
    offset = 56 # int | Number of initial records to skip (optional)
    search = 'search_example' # str | Case insensitive search against domain names (optional)

    try:
        # List Domains
        api_response = api_instance.get_all_domains(limit=limit, offset=offset, search=search)
        print("The response of DomainApi->get_all_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainApi->get_all_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of records to return per request | [optional] 
 **offset** | **int**| Number of initial records to skip | [optional] 
 **search** | **str**| Case insensitive search against domain names | [optional] 

### Return type

[**List[Domain]**](Domain.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of domains retrieved successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subaccount_domain_domain_id_delete**
> DeleteResponse subaccount_domain_domain_id_delete(domain_id)

Delete Domain

Delete a specific domain using its `id`.

### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.delete_response import DeleteResponse
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
    api_instance = sendpost_python_sdk.DomainApi(api_client)
    domain_id = 'domain_id_example' # str | The unique ID of the domain to delete.

    try:
        # Delete Domain
        api_response = api_instance.subaccount_domain_domain_id_delete(domain_id)
        print("The response of DomainApi->subaccount_domain_domain_id_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainApi->subaccount_domain_domain_id_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The unique ID of the domain to delete. | 

### Return type

[**DeleteResponse**](DeleteResponse.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subaccount_domain_domain_id_get**
> Domain subaccount_domain_domain_id_get(domain_id)

Get Domain

Retrieve details of a specific domain using its `id`.

### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.domain import Domain
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
    api_instance = sendpost_python_sdk.DomainApi(api_client)
    domain_id = 'domain_id_example' # str | The unique ID of the domain to retrieve.

    try:
        # Get Domain
        api_response = api_instance.subaccount_domain_domain_id_get(domain_id)
        print("The response of DomainApi->subaccount_domain_domain_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainApi->subaccount_domain_domain_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domain_id** | **str**| The unique ID of the domain to retrieve. | 

### Return type

[**Domain**](Domain.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **subaccount_domain_post**
> Domain subaccount_domain_post(create_domain_request)

Create Domain

Add a new domain using its `name`.

### Example

* Api Key Authentication (subAccountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.create_domain_request import CreateDomainRequest
from sendpost_python_sdk.models.domain import Domain
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
    api_instance = sendpost_python_sdk.DomainApi(api_client)
    create_domain_request = sendpost_python_sdk.CreateDomainRequest() # CreateDomainRequest | 

    try:
        # Create Domain
        api_response = api_instance.subaccount_domain_post(create_domain_request)
        print("The response of DomainApi->subaccount_domain_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DomainApi->subaccount_domain_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_domain_request** | [**CreateDomainRequest**](CreateDomainRequest.md)|  | 

### Return type

[**Domain**](Domain.md)

### Authorization

[subAccountAuth](../README.md#subAccountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

