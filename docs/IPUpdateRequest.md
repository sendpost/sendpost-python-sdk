# IPUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auto_warmup_enabled** | **bool** | Whether the IP warmup should happen automatically or be managed manually | 

## Example

```python
from sendpost-python-sdk.models.ip_update_request import IPUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IPUpdateRequest from a JSON string
ip_update_request_instance = IPUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(IPUpdateRequest.to_json())

# convert the object into a dict
ip_update_request_dict = ip_update_request_instance.to_dict()
# create an instance of IPUpdateRequest from a dict
ip_update_request_from_dict = IPUpdateRequest.from_dict(ip_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


