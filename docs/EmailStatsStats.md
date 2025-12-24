# EmailStatsStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**processed** | **int** | Number of emails accepted by SendPost API | [optional] 
**sent** | **int** | Number of emails sent | [optional] 
**delivered** | **int** | Number of emails successfully delivered to SMTP without errors | [optional] 
**dropped** | **int** | Number of emails dropped without attempting to deliver due to invalid email or suppression list | [optional] 
**smtp_dropped** | **int** | Number of emails dropped by SMTP | [optional] 
**hard_bounced** | **int** | Number of emails that resulted in a hard bounce error | [optional] 
**soft_bounced** | **int** | Number of emails that resulted in a temporary soft bounce error | [optional] 
**opened** | **int** | Number of emails opened by recipients | [optional] 
**clicked** | **int** | Number of email links clicked by recipients | [optional] 
**unsubscribed** | **int** | Number of email recipients who unsubscribed | [optional] 
**spam** | **int** | Number of emails marked as spam by recipients | [optional] 

## Example

```python
from sendpost-python-sdk.models.email_stats_stats import EmailStatsStats

# TODO update the JSON string below
json = "{}"
# create an instance of EmailStatsStats from a JSON string
email_stats_stats_instance = EmailStatsStats.from_json(json)
# print the JSON string representation of the object
print(EmailStatsStats.to_json())

# convert the object into a dict
email_stats_stats_dict = email_stats_stats_instance.to_dict()
# create an instance of EmailStatsStats from a dict
email_stats_stats_from_dict = EmailStatsStats.from_dict(email_stats_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


