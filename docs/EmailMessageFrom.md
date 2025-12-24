# EmailMessageFrom


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.email_message_from import EmailMessageFrom

# TODO update the JSON string below
json = "{}"
# create an instance of EmailMessageFrom from a JSON string
email_message_from_instance = EmailMessageFrom.from_json(json)
# print the JSON string representation of the object
print(EmailMessageFrom.to_json())

# convert the object into a dict
email_message_from_dict = email_message_from_instance.to_dict()
# create an instance of EmailMessageFrom from a dict
email_message_from_from_dict = EmailMessageFrom.from_dict(email_message_from_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


