# IPPoolDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.ip_pool_delete_response import IPPoolDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IPPoolDeleteResponse from a JSON string
ip_pool_delete_response_instance = IPPoolDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(IPPoolDeleteResponse.to_json())

# convert the object into a dict
ip_pool_delete_response_dict = ip_pool_delete_response_instance.to_dict()
# create an instance of IPPoolDeleteResponse from a dict
ip_pool_delete_response_from_dict = IPPoolDeleteResponse.from_dict(ip_pool_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


