# IPPoolCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**ips** | [**List[EIP]**](EIP.md) |  | [optional] 
**tpsps** | **List[int]** |  | [optional] 
**routing_strategy** | **int** |  | [optional] 
**routing_meta_data** | **str** |  | [optional] 
**overflow_pool** | **bool** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.ip_pool_create_request import IPPoolCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IPPoolCreateRequest from a JSON string
ip_pool_create_request_instance = IPPoolCreateRequest.from_json(json)
# print the JSON string representation of the object
print(IPPoolCreateRequest.to_json())

# convert the object into a dict
ip_pool_create_request_dict = ip_pool_create_request_instance.to_dict()
# create an instance of IPPoolCreateRequest from a dict
ip_pool_create_request_from_dict = IPPoolCreateRequest.from_dict(ip_pool_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


