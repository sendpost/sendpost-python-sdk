# CopyTo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**custom_fields** | **Dict[str, object]** | Custom fields for personalization | [optional] 

## Example

```python
from sendpost-python-sdk.models.copy_to import CopyTo

# TODO update the JSON string below
json = "{}"
# create an instance of CopyTo from a JSON string
copy_to_instance = CopyTo.from_json(json)
# print the JSON string representation of the object
print(CopyTo.to_json())

# convert the object into a dict
copy_to_dict = copy_to_instance.to_dict()
# create an instance of CopyTo from a dict
copy_to_from_dict = CopyTo.from_dict(copy_to_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


