# sendpost-python-sdk.StatsApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**account_subaccount_stat_subaccount_id_aggregate_get**](StatsApi.md#account_subaccount_stat_subaccount_id_aggregate_get) | **GET** /account/subaccount/stat/{subaccount_id}/aggregate | Get Aggregate Stats
[**account_subaccount_stat_subaccount_id_get**](StatsApi.md#account_subaccount_stat_subaccount_id_get) | **GET** /account/subaccount/stat/{subaccount_id} | List Stats
[**get_aggregate_stats_by_group**](StatsApi.md#get_aggregate_stats_by_group) | **GET** /account/subaccount/stat/{subaccount_id}/group | Get Group Aggregate Stats


# **account_subaccount_stat_subaccount_id_aggregate_get**
> AggregateStat account_subaccount_stat_subaccount_id_aggregate_get(var_from, to, subaccount_id)

Get Aggregate Stats

Retrieves aggregated email stats for a specific sub-account for a date range.   **Note**: The maximum date range is 366 days.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.aggregate_stat import AggregateStat
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
    api_instance = sendpost-python-sdk.StatsApi(api_client)
    var_from = '2013-10-20' # date | Start date for stats retrieval.
    to = '2013-10-20' # date | Date to which stats should be retrieved ( Note than from date should be earlier than to date. Also the difference between from and to date shouldn't ne more than 60 days ) 
    subaccount_id = 11 # int | The ID of the subaccount to retrieve

    try:
        # Get Aggregate Stats
        api_response = api_instance.account_subaccount_stat_subaccount_id_aggregate_get(var_from, to, subaccount_id)
        print("The response of StatsApi->account_subaccount_stat_subaccount_id_aggregate_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsApi->account_subaccount_stat_subaccount_id_aggregate_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **date**| Start date for stats retrieval. | 
 **to** | **date**| Date to which stats should be retrieved ( Note than from date should be earlier than to date. Also the difference between from and to date shouldn&#39;t ne more than 60 days )  | 
 **subaccount_id** | **int**| The ID of the subaccount to retrieve | 

### Return type

[**AggregateStat**](AggregateStat.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **account_subaccount_stat_subaccount_id_get**
> List[Stat] account_subaccount_stat_subaccount_id_get(var_from, to, subaccount_id)

List Stats

Retrieves a list of email stats for a specific sub-account within a given date range. Both `from` and `to` dates are inclusive.   **Note**: The maximum date range is 31 days.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.stat import Stat
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
    api_instance = sendpost-python-sdk.StatsApi(api_client)
    var_from = '2013-10-20' # date | Start date for stats retrieval.
    to = '2013-10-20' # date | Date to which stats should be retrieved ( Note than from date should be earlier than to date. Also the difference between from and to date shouldn't ne more than 60 days ) 
    subaccount_id = 11 # int | The ID of the subaccount to retrieve

    try:
        # List Stats
        api_response = api_instance.account_subaccount_stat_subaccount_id_get(var_from, to, subaccount_id)
        print("The response of StatsApi->account_subaccount_stat_subaccount_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsApi->account_subaccount_stat_subaccount_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **date**| Start date for stats retrieval. | 
 **to** | **date**| Date to which stats should be retrieved ( Note than from date should be earlier than to date. Also the difference between from and to date shouldn&#39;t ne more than 60 days )  | 
 **subaccount_id** | **int**| The ID of the subaccount to retrieve | 

### Return type

[**List[Stat]**](Stat.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_aggregate_stats_by_group**
> AggregateStat get_aggregate_stats_by_group(group, var_from, to, subaccount_id)

Get Group Aggregate Stats

Retrieves aggregated email stats for a specific group in a sub-account for the specified daterange.
The maximum daterange for which these stats can be retrieved is 366 days. Ensure that the difference between the `from` and `to` dates does not exceed 366 days.


### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.aggregate_stat import AggregateStat
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
    api_instance = sendpost-python-sdk.StatsApi(api_client)
    group = 'group_example' # str | Group whose aggregated stats need to be retrieved
    var_from = '2013-10-20' # date | The starting date for the aggregated stats
    to = '2013-10-20' # date | The ending date for the aggregated stats (Note: `from` should be earlier than `to` and the date range should not exceed 366 days) 
    subaccount_id = 11 # int | The ID of the subaccount to retrieve

    try:
        # Get Group Aggregate Stats
        api_response = api_instance.get_aggregate_stats_by_group(group, var_from, to, subaccount_id)
        print("The response of StatsApi->get_aggregate_stats_by_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsApi->get_aggregate_stats_by_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **str**| Group whose aggregated stats need to be retrieved | 
 **var_from** | **date**| The starting date for the aggregated stats | 
 **to** | **date**| The ending date for the aggregated stats (Note: &#x60;from&#x60; should be earlier than &#x60;to&#x60; and the date range should not exceed 366 days)  | 
 **subaccount_id** | **int**| The ID of the subaccount to retrieve | 

### Return type

[**AggregateStat**](AggregateStat.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Aggregated email stats for the group within the specified date range |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

