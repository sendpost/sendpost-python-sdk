# UpdateSubAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | New name for the sub-account. | [optional] 

## Example

```python
from sendpost_python_sdk.models.update_sub_account import UpdateSubAccount

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSubAccount from a JSON string
update_sub_account_instance = UpdateSubAccount.from_json(json)
# print the JSON string representation of the object
print(UpdateSubAccount.to_json())

# convert the object into a dict
update_sub_account_dict = update_sub_account_instance.to_dict()
# create an instance of UpdateSubAccount from a dict
update_sub_account_from_dict = UpdateSubAccount.from_dict(update_sub_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


