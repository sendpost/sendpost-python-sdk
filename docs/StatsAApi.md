# sendpost-python-sdk.StatsAApi

All URIs are relative to *https://api.sendpost.io/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account_aggregate_stats**](StatsAApi.md#get_account_aggregate_stats) | **GET** /account/stat/aggregate | Get Account Aggregate Stats
[**get_account_aggregate_stats_by_group**](StatsAApi.md#get_account_aggregate_stats_by_group) | **GET** /account/stat/aggregate/group | Get Account Group Aggregate Stats
[**get_account_stats_by_group**](StatsAApi.md#get_account_stats_by_group) | **GET** /account/stat/group | List Account Group Stats
[**get_all_account_stats**](StatsAApi.md#get_all_account_stats) | **GET** /account/stat | List Account Stats


# **get_account_aggregate_stats**
> AggregateStats get_account_aggregate_stats(var_from, to)

Get Account Aggregate Stats

Retrieve aggregated email statistics for all sub-accounts of a specific account for a given date range.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.aggregate_stats import AggregateStats
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
    api_instance = sendpost-python-sdk.StatsAApi(api_client)
    var_from = '2019-01-01' # date | The start date for retrieving aggregated stats (inclusive)
    to = '2019-12-31' # date | The end date for retrieving aggregated stats (inclusive). The difference between `from` and `to` should not exceed 366 days.

    try:
        # Get Account Aggregate Stats
        api_response = api_instance.get_account_aggregate_stats(var_from, to)
        print("The response of StatsAApi->get_account_aggregate_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsAApi->get_account_aggregate_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **date**| The start date for retrieving aggregated stats (inclusive) | 
 **to** | **date**| The end date for retrieving aggregated stats (inclusive). The difference between &#x60;from&#x60; and &#x60;to&#x60; should not exceed 366 days. | 

### Return type

[**AggregateStats**](AggregateStats.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Aggregated statistics for the specified date range. |  -  |
**400** | Bad request, invalid date range |  -  |
**401** | Unauthorized, invalid API key |  -  |
**404** | Data not found for the given date range |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_aggregate_stats_by_group**
> AggregateStat get_account_aggregate_stats_by_group(group, var_from, to)

Get Account Group Aggregate Stats

Gets aggregated email stats for a specific group in all sub-accounts of a specific account for the given daterange. The maximum daterange for which these stats can be retrieved is 366 days.

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
    api_instance = sendpost-python-sdk.StatsAApi(api_client)
    group = 'shopify' # str | Group whose aggregate stats need to be retrieved.
    var_from = '2019-01-01' # date | Date from which stats should be retrieved (should be in the format `YYYY-MM-DD`).
    to = '2019-12-31' # date | Date to which stats should be retrieved (should be in the format `YYYY-MM-DD`). Note that the difference between `from` and `to` should not be more than 366 days.

    try:
        # Get Account Group Aggregate Stats
        api_response = api_instance.get_account_aggregate_stats_by_group(group, var_from, to)
        print("The response of StatsAApi->get_account_aggregate_stats_by_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsAApi->get_account_aggregate_stats_by_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **str**| Group whose aggregate stats need to be retrieved. | 
 **var_from** | **date**| Date from which stats should be retrieved (should be in the format &#x60;YYYY-MM-DD&#x60;). | 
 **to** | **date**| Date to which stats should be retrieved (should be in the format &#x60;YYYY-MM-DD&#x60;). Note that the difference between &#x60;from&#x60; and &#x60;to&#x60; should not be more than 366 days. | 

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
**200** | Successfully retrieved aggregate stats by group. |  -  |
**400** | Bad Request, invalid query parameters. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_stats_by_group**
> List[Stat] get_account_stats_by_group(group, var_from, to)

List Account Group Stats

Gets a list of all email stats for all sub-accounts of a specific account by group for a given daterange. The maximum daterange for which these stats can be retrieved is 31 days.

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
    api_instance = sendpost-python-sdk.StatsAApi(api_client)
    group = 'shopify' # str | Group whose stats need to be retrieved
    var_from = '2020-03-12' # date | Date from which stats should be retrieved (should be in the format `YYYY-MM-DD`)
    to = '2020-04-14' # date | Date to which stats should be retrieved (should be in the format `YYYY-MM-DD`). Note that the difference between `from` and `to` should not be more than 31 days.

    try:
        # List Account Group Stats
        api_response = api_instance.get_account_stats_by_group(group, var_from, to)
        print("The response of StatsAApi->get_account_stats_by_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsAApi->get_account_stats_by_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **str**| Group whose stats need to be retrieved | 
 **var_from** | **date**| Date from which stats should be retrieved (should be in the format &#x60;YYYY-MM-DD&#x60;) | 
 **to** | **date**| Date to which stats should be retrieved (should be in the format &#x60;YYYY-MM-DD&#x60;). Note that the difference between &#x60;from&#x60; and &#x60;to&#x60; should not be more than 31 days. | 

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
**200** | Successfully retrieved stats by group. |  -  |
**400** | Bad Request, invalid query parameters. |  -  |
**401** | Unauthorized, invalid API key. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_account_stats**
> List[AccountStats] get_all_account_stats(var_from, to)

List Account Stats

Retrieve email statistics for all sub-accounts of a specific account for a given date range.

### Example

* Api Key Authentication (accountAuth):

```python
import sendpost-python-sdk
from sendpost-python-sdk.models.account_stats import AccountStats
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
    api_instance = sendpost-python-sdk.StatsAApi(api_client)
    var_from = '2020-03-12' # date | The start date for retrieving stats (inclusive)
    to = '2020-04-14' # date | The end date for retrieving stats (inclusive). The difference between `from` and `to` should not exceed 31 days.

    try:
        # List Account Stats
        api_response = api_instance.get_all_account_stats(var_from, to)
        print("The response of StatsAApi->get_all_account_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling StatsAApi->get_all_account_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **date**| The start date for retrieving stats (inclusive) | 
 **to** | **date**| The end date for retrieving stats (inclusive). The difference between &#x60;from&#x60; and &#x60;to&#x60; should not exceed 31 days. | 

### Return type

[**List[AccountStats]**](AccountStats.md)

### Authorization

[accountAuth](../README.md#accountAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of statistics for the specified date range. |  -  |
**400** | Bad request, invalid date range |  -  |
**401** | Unauthorized, invalid API key |  -  |
**404** | Data not found for the given date range |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

