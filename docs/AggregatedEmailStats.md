# AggregatedEmailStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**processed** | **int** | Total number of emails accepted by SendPost API | [optional] 
**sent** | **int** | Total number of emails sent | [optional] 
**delivered** | **int** | Total number of emails successfully delivered to SMTP | [optional] 
**dropped** | **int** | Total number of emails dropped without delivery | [optional] 
**smtp_dropped** | **int** | Total number of emails dropped by SMTP | [optional] 
**hard_bounced** | **int** | Total number of hard bounce errors | [optional] 
**soft_bounced** | **int** | Total number of soft bounce errors | [optional] 
**opened** | **int** | Total number of emails opened by recipients | [optional] 
**clicked** | **int** | Total number of links clicked by recipients | [optional] 
**unsubscribed** | **int** | Total number of unsubscribed recipients | [optional] 
**spam** | **int** | Total number of spams reported by recipients | [optional] 

## Example

```python
from sendpost_python_sdk.models.aggregated_email_stats import AggregatedEmailStats

# TODO update the JSON string below
json = "{}"
# create an instance of AggregatedEmailStats from a JSON string
aggregated_email_stats_instance = AggregatedEmailStats.from_json(json)
# print the JSON string representation of the object
print(AggregatedEmailStats.to_json())

# convert the object into a dict
aggregated_email_stats_dict = aggregated_email_stats_instance.to_dict()
# create an instance of AggregatedEmailStats from a dict
aggregated_email_stats_from_dict = AggregatedEmailStats.from_dict(aggregated_email_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


