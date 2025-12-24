# AggregateStats


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
from sendpost-python-sdk.models.aggregate_stats import AggregateStats

# TODO update the JSON string below
json = "{}"
# create an instance of AggregateStats from a JSON string
aggregate_stats_instance = AggregateStats.from_json(json)
# print the JSON string representation of the object
print(AggregateStats.to_json())

# convert the object into a dict
aggregate_stats_dict = aggregate_stats_instance.to_dict()
# create an instance of AggregateStats from a dict
aggregate_stats_from_dict = AggregateStats.from_dict(aggregate_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


