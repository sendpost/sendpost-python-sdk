# MessageHeaderTo

Header To recipient object comprising name, email, cc, bcc and customFields

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
from sendpost_python_sdk.models.message_header_to import MessageHeaderTo

# TODO update the JSON string below
json = "{}"
# create an instance of MessageHeaderTo from a JSON string
message_header_to_instance = MessageHeaderTo.from_json(json)
# print the JSON string representation of the object
print(MessageHeaderTo.to_json())

# convert the object into a dict
message_header_to_dict = message_header_to_instance.to_dict()
# create an instance of MessageHeaderTo from a dict
message_header_to_from_dict = MessageHeaderTo.from_dict(message_header_to_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


