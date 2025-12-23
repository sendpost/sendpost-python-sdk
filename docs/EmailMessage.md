# EmailMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | **str** |  | [optional] 
**account_id** | **int** |  | [optional] 
**sub_account_id** | **int** |  | [optional] 
**ip_id** | **int** |  | [optional] 
**public_ip** | **str** |  | [optional] 
**local_ip** | **str** |  | [optional] 
**email_type** | **str** |  | [optional] 
**submitted_at** | **int** |  | [optional] 
**var_from** | [**EmailMessageFrom**](EmailMessageFrom.md) |  | [optional] 
**reply_to** | [**EmailMessageReplyTo**](EmailMessageReplyTo.md) |  | [optional] 
**to** | [**List[EmailMessageToInner]**](EmailMessageToInner.md) |  | [optional] 
**groups** | **List[str]** |  | [optional] 
**ip_pool** | **str** |  | [optional] 
**headers** | **Dict[str, str]** |  | [optional] 
**custom_fields** | **Dict[str, str]** |  | [optional] 
**track_opens** | **bool** |  | [optional] 
**track_clicks** | **bool** |  | [optional] 
**webhook_endpoint** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.email_message import EmailMessage

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessage from a JSON string
email_message_instance = EmailMessage.from_json(json)
# print the JSON string representation of the object
print(EmailMessage.to_json())

# convert the object into a dict
email_message_dict = email_message_instance.to_dict()
# create an instance of EmailMessage from a dict
email_message_from_dict = EmailMessage.from_dict(email_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


