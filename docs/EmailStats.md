# EmailStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | The UTC date for which stats are retrieved | [optional] 
**stats** | [**EmailStatsStats**](EmailStatsStats.md) |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.email_stats import EmailStats

# TODO update the JSON string below
json = "{}"
# create an instance of EmailStats from a JSON string
email_stats_instance = EmailStats.from_json(json)
# print the JSON string representation of the object
print(EmailStats.to_json())

# convert the object into a dict
email_stats_dict = email_stats_instance.to_dict()
# create an instance of EmailStats from a dict
email_stats_from_dict = EmailStats.from_dict(email_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


