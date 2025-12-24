# EmailMessageWithTemplate


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
**template** | **str** |  | [optional] 
**template_id** | **str** | Template ID for the email template | [optional] 
**template_variables** | **Dict[str, str]** | Key-Value pair of template variables | [optional] 

## Example

```python
from sendpost_python_sdk.models.email_message_with_template import EmailMessageWithTemplate

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessageWithTemplate from a JSON string
email_message_with_template_instance = EmailMessageWithTemplate.from_json(json)
# print the JSON string representation of the object
print(EmailMessageWithTemplate.to_json())

# convert the object into a dict
email_message_with_template_dict = email_message_with_template_instance.to_dict()
# create an instance of EmailMessageWithTemplate from a dict
email_message_with_template_from_dict = EmailMessageWithTemplate.from_dict(email_message_with_template_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


