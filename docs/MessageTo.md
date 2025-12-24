# MessageTo

Recipient object comprising name, email, cc, bcc and customFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the recipient. | [optional] 
**email** | **str** | Email address of the recipient. | [optional] 
**cc** | **List[str]** | List of CC recipients | [optional] 
**bcc** | **List[str]** | List of BCC recipients | [optional] 
**custom_fields** | **Dict[str, str]** | Key-Value pair of custom fields. | [optional] 

## Example

```python
from sendpost-python-sdk.models.message_to import MessageTo

# TODO update the JSON string below
json = "{}"
# create an instance of MessageTo from a JSON string
message_to_instance = MessageTo.from_json(json)
# print the JSON string representation of the object
print(MessageTo.to_json())

# convert the object into a dict
message_to_dict = message_to_instance.to_dict()
# create an instance of MessageTo from a dict
message_to_from_dict = MessageTo.from_dict(message_to_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


