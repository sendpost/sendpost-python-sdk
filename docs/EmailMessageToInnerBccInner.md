# EmailMessageToInnerBccInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**custom_fields** | **Dict[str, str]** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.email_message_to_inner_bcc_inner import EmailMessageToInnerBccInner

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessageToInnerBccInner from a JSON string
email_message_to_inner_bcc_inner_instance = EmailMessageToInnerBccInner.from_json(json)
# print the JSON string representation of the object
print(EmailMessageToInnerBccInner.to_json())

# convert the object into a dict
email_message_to_inner_bcc_inner_dict = email_message_to_inner_bcc_inner_instance.to_dict()
# create an instance of EmailMessageToInnerBccInner from a dict
email_message_to_inner_bcc_inner_from_dict = EmailMessageToInnerBccInner.from_dict(email_message_to_inner_bcc_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


