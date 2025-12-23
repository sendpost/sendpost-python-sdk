# DeleteSuppression200ResponseInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The ID of the deleted suppression | [optional] 
**message** | **str** | A success message after the suppression(s) are deleted | [optional] 

## Example

```python
from sendpost_python_sdk.models.delete_suppression200_response_inner import DeleteSuppression200ResponseInner

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteSuppression200ResponseInner from a JSON string
delete_suppression200_response_inner_instance = DeleteSuppression200ResponseInner.from_json(json)
# print the JSON string representation of the object
print(DeleteSuppression200ResponseInner.to_json())

# convert the object into a dict
delete_suppression200_response_inner_dict = delete_suppression200_response_inner_instance.to_dict()
# create an instance of DeleteSuppression200ResponseInner from a dict
delete_suppression200_response_inner_from_dict = DeleteSuppression200ResponseInner.from_dict(delete_suppression200_response_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


