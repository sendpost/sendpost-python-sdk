# IPDeletionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The unique ID of the IP | 
**message** | **str** | The confirmation message after deletion | 

## Example

```python
from sendpost_python_sdk.models.ip_deletion_response import IPDeletionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IPDeletionResponse from a JSON string
ip_deletion_response_instance = IPDeletionResponse.from_json(json)
# print the JSON string representation of the object
print(IPDeletionResponse.to_json())

# convert the object into a dict
ip_deletion_response_dict = ip_deletion_response_instance.to_dict()
# create an instance of IPDeletionResponse from a dict
ip_deletion_response_from_dict = IPDeletionResponse.from_dict(ip_deletion_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


