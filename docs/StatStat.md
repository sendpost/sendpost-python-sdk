# StatStat

Statistics data for the date

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**processed** | **int** | Number of emails accepted by SendPost API. | [optional] 
**sent** | **int** | Number of emails sent. | [optional] 
**delivered** | **int** | Number of emails we were able to successfully deliver at SMTP without encountering any error | [optional] 
**dropped** | **int** | Number of emails drop without attempting to deliver either because the email is invalid or email in in existing suppression list | [optional] 
**smtp_dropped** | **int** | Number of emails dropped by SMTP. | [optional] 
**hard_bounced** | **int** | Number of emails where we got SMTP hard bounce error code by the recipient mail provider | [optional] 
**soft_bounced** | **int** | Number of emails where we got temporary soft bounce error by the recipent mail provider. Soft bounced emails are retried upto 5 times over 24 hour period before marking them as hardBounced. | [optional] 
**opened** | **int** | Number of emails opened by recipients | [optional] 
**clicked** | **int** | Number of email links clicked by recipients | [optional] 
**unsubscribed** | **int** | Number of email recipients who unsubscribed from receiving further emails | [optional] 
**spam** | **int** | Number of email recipients who marked emails as spam | [optional] 

## Example

```python
from sendpost_python_sdk.models.stat_stat import StatStat

# TODO update the JSON string below
json = "{}"
# create an instance of StatStat from a JSON string
stat_stat_instance = StatStat.from_json(json)
# print the JSON string representation of the object
print(StatStat.to_json())

# convert the object into a dict
stat_stat_dict = stat_stat_instance.to_dict()
# create an instance of StatStat from a dict
stat_stat_from_dict = StatStat.from_dict(stat_stat_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


