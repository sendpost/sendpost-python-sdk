# AccountStatsStat


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**processed** | **int** |  | [optional] 
**sent** | **int** |  | [optional] 
**delivered** | **int** |  | [optional] 
**dropped** | **int** |  | [optional] 
**smtp_dropped** | **int** |  | [optional] 
**hard_bounced** | **int** |  | [optional] 
**soft_bounced** | **int** |  | [optional] 
**opened** | **int** |  | [optional] 
**clicked** | **int** |  | [optional] 
**unsubscribed** | **int** |  | [optional] 
**spams** | **int** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.account_stats_stat import AccountStatsStat

# TODO update the JSON string below
json = "{}"
# create an instance of AccountStatsStat from a JSON string
account_stats_stat_instance = AccountStatsStat.from_json(json)
# print the JSON string representation of the object
print(AccountStatsStat.to_json())

# convert the object into a dict
account_stats_stat_dict = account_stats_stat_instance.to_dict()
# create an instance of AccountStatsStat from a dict
account_stats_stat_from_dict = AccountStatsStat.from_dict(account_stats_stat_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


