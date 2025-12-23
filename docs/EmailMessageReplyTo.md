# EmailMessageReplyTo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.email_message_reply_to import EmailMessageReplyTo

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessageReplyTo from a JSON string
email_message_reply_to_instance = EmailMessageReplyTo.from_json(json)
# print the JSON string representation of the object
print(EmailMessageReplyTo.to_json())

# convert the object into a dict
email_message_reply_to_dict = email_message_reply_to_instance.to_dict()
# create an instance of EmailMessageReplyTo from a dict
email_message_reply_to_from_dict = EmailMessageReplyTo.from_dict(email_message_reply_to_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


