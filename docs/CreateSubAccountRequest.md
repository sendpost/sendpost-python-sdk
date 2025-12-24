# CreateSubAccountRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name for the new sub-account. | [optional] 

## Example

```python
from sendpost_python_sdk.models.create_sub_account_request import CreateSubAccountRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSubAccountRequest from a JSON string
create_sub_account_request_instance = CreateSubAccountRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSubAccountRequest.to_json())

# convert the object into a dict
create_sub_account_request_dict = create_sub_account_request_instance.to_dict()
# create an instance of CreateSubAccountRequest from a dict
create_sub_account_request_from_dict = CreateSubAccountRequest.from_dict(create_sub_account_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


