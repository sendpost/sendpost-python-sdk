# Recipient


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**cc** | [**List[CopyTo]**](CopyTo.md) |  | [optional] 
**bcc** | [**List[CopyTo]**](CopyTo.md) |  | [optional] 
**custom_fields** | **Dict[str, object]** | Custom fields for personalization | [optional] 

## Example

```python
from sendpost_python_sdk.models.recipient import Recipient

# TODO update the JSON string below
json = "{}"
# create an instance of Recipient from a JSON string
recipient_instance = Recipient.from_json(json)
# print the JSON string representation of the object
print(Recipient.to_json())

# convert the object into a dict
recipient_dict = recipient_instance.to_dict()
# create an instance of Recipient from a dict
recipient_from_dict = Recipient.from_dict(recipient_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


