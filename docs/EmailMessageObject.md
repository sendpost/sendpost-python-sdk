# EmailMessageObject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_from** | [**EmailAddress**](EmailAddress.md) |  | [optional] 
**reply_to** | [**EmailAddress**](EmailAddress.md) |  | [optional] 
**to** | [**List[Recipient]**](Recipient.md) |  | [optional] 
**subject** | **str** |  | [optional] 
**pre_text** | **str** |  | [optional] 
**html_body** | **str** |  | [optional] 
**text_body** | **str** |  | [optional] 
**amp_body** | **str** |  | [optional] 
**ippool** | **str** |  | [optional] 
**headers** | **Dict[str, str]** |  | [optional] 
**track_opens** | **bool** |  | [optional] 
**track_clicks** | **bool** |  | [optional] 
**groups** | **List[str]** |  | [optional] 
**attachments** | [**List[Attachment]**](Attachment.md) |  | [optional] 
**webhook_endpoint** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.email_message_object import EmailMessageObject

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessageObject from a JSON string
email_message_object_instance = EmailMessageObject.from_json(json)
# print the JSON string representation of the object
print(EmailMessageObject.to_json())

# convert the object into a dict
email_message_object_dict = email_message_object_instance.to_dict()
# create an instance of EmailMessageObject from a dict
email_message_object_from_dict = EmailMessageObject.from_dict(email_message_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


