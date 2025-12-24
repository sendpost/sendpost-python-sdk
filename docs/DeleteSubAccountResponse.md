# DeleteSubAccountResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the deleted sub-account. | [optional] 
**message** | **str** | Message confirming the deletion. | [optional] 

## Example

```python
from sendpost-python-sdk.models.delete_sub_account_response import DeleteSubAccountResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteSubAccountResponse from a JSON string
delete_sub_account_response_instance = DeleteSubAccountResponse.from_json(json)
# print the JSON string representation of the object
print(DeleteSubAccountResponse.to_json())

# convert the object into a dict
delete_sub_account_response_dict = delete_sub_account_response_instance.to_dict()
# create an instance of DeleteSubAccountResponse from a dict
delete_sub_account_response_from_dict = DeleteSubAccountResponse.from_dict(delete_sub_account_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


