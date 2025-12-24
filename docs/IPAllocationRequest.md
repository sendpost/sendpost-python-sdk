# IPAllocationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**overflow_pool** | **bool** | Determines whether emails should be sent over shared IP when the IP pool is full | 
**ips** | **List[str]** |  | 

## Example

```python
from sendpost-python-sdk.models.ip_allocation_request import IPAllocationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IPAllocationRequest from a JSON string
ip_allocation_request_instance = IPAllocationRequest.from_json(json)
# print the JSON string representation of the object
print(IPAllocationRequest.to_json())

# convert the object into a dict
ip_allocation_request_dict = ip_allocation_request_instance.to_dict()
# create an instance of IPAllocationRequest from a dict
ip_allocation_request_from_dict = IPAllocationRequest.from_dict(ip_allocation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


