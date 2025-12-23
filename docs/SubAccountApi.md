# sendpost_python_sdk.SubAccountApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sub_account**](SubAccountApi.md#create_sub_account) | **POST** /account/subaccount/ | Create Sub-Account
[**delete_sub_account**](SubAccountApi.md#delete_sub_account) | **DELETE** /account/subaccount/{subaccount_id} | Delete Sub-Account
[**get_all_sub_accounts**](SubAccountApi.md#get_all_sub_accounts) | **GET** /account/subaccount/ | List Sub-Accounts
[**get_sub_account**](SubAccountApi.md#get_sub_account) | **GET** /account/subaccount/{subaccount_id} | Get Sub-Account
[**update_sub_account**](SubAccountApi.md#update_sub_account) | **PUT** /account/subaccount/{subaccount_id} | Update Sub-Account


# **create_sub_account**
> SubAccount create_sub_account(create_sub_account_request)

Create Sub-Account

Creates a new sub-account under the current account.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.create_sub_account_request import CreateSubAccountRequest
from sendpost_python_sdk.models.sub_account import SubAccount
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
    api_instance = sendpost_python_sdk.SubAccountApi(api_client)
    create_sub_account_request = sendpost_python_sdk.CreateSubAccountRequest() # CreateSubAccountRequest | 

    try:
        # Create Sub-Account
        api_response = api_instance.create_sub_account(create_sub_account_request)
        print("The response of SubAccountApi->create_sub_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubAccountApi->create_sub_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_sub_account_request** | [**CreateSubAccountRequest**](CreateSubAccountRequest.md)|  | 

### Return type

[**SubAccount**](SubAccount.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Sub-account successfully created. |  -  |
**403** | Forbidden, sub-account with the same name already exists. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_sub_account**
> DeleteSubAccountResponse delete_sub_account(subaccount_id)

Delete Sub-Account

Deletes a specific sub-account by its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.delete_sub_account_response import DeleteSubAccountResponse
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
    api_instance = sendpost_python_sdk.SubAccountApi(api_client)
    subaccount_id = 12 # int | The ID of the sub-account to delete.

    try:
        # Delete Sub-Account
        api_response = api_instance.delete_sub_account(subaccount_id)
        print("The response of SubAccountApi->delete_sub_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubAccountApi->delete_sub_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subaccount_id** | **int**| The ID of the sub-account to delete. | 

### Return type

[**DeleteSubAccountResponse**](DeleteSubAccountResponse.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Sub-account successfully deleted. |  -  |
**406** | Not Acceptable. Cannot delete the default sub-account. |  -  |
**401** | Unauthorized. Invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_sub_accounts**
> List[SubAccount] get_all_sub_accounts(limit=limit, offset=offset, search=search)

List Sub-Accounts

Retrieves a list of all sub-accounts associated with a specific account.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.sub_account import SubAccount
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
    api_instance = sendpost_python_sdk.SubAccountApi(api_client)
    limit = 10 # int | Number of records to return per request. (optional)
    offset = 0 # int | Number of initial records to skip. (optional)
    search = 'Hooli' # str | Case-insensitive search against the sub-account name. (optional)

    try:
        # List Sub-Accounts
        api_response = api_instance.get_all_sub_accounts(limit=limit, offset=offset, search=search)
        print("The response of SubAccountApi->get_all_sub_accounts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubAccountApi->get_all_sub_accounts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of records to return per request. | [optional] 
 **offset** | **int**| Number of initial records to skip. | [optional] 
 **search** | **str**| Case-insensitive search against the sub-account name. | [optional] 

### Return type

[**List[SubAccount]**](SubAccount.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully retrieved sub-accounts. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sub_account**
> SubAccount get_sub_account(subaccount_id)

Get Sub-Account

Retrieves a specific sub-account by its ID.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.sub_account import SubAccount
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
    api_instance = sendpost_python_sdk.SubAccountApi(api_client)
    subaccount_id = 11 # int | The ID of the sub-account to retrieve.

    try:
        # Get Sub-Account
        api_response = api_instance.get_sub_account(subaccount_id)
        print("The response of SubAccountApi->get_sub_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubAccountApi->get_sub_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subaccount_id** | **int**| The ID of the sub-account to retrieve. | 

### Return type

[**SubAccount**](SubAccount.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully retrieved the sub-account. |  -  |
**404** | Sub-account not found. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sub_account**
> SubAccount update_sub_account(subaccount_id, update_sub_account)

Update Sub-Account

Updates the details of an existing sub-account.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost_python_sdk
from sendpost_python_sdk.models.sub_account import SubAccount
from sendpost_python_sdk.models.update_sub_account import UpdateSubAccount
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
    api_instance = sendpost_python_sdk.SubAccountApi(api_client)
    subaccount_id = 12 # int | The ID of the sub-account to update.
    update_sub_account = sendpost_python_sdk.UpdateSubAccount() # UpdateSubAccount | 

    try:
        # Update Sub-Account
        api_response = api_instance.update_sub_account(subaccount_id, update_sub_account)
        print("The response of SubAccountApi->update_sub_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubAccountApi->update_sub_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subaccount_id** | **int**| The ID of the sub-account to update. | 
 **update_sub_account** | [**UpdateSubAccount**](UpdateSubAccount.md)|  | 

### Return type

[**SubAccount**](SubAccount.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Sub-account successfully updated. |  -  |
**404** | Sub-account not found. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

