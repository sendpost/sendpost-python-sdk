# IPPoolUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**ips** | [**List[IP]**](IP.md) |  | [optional] 
**routing_strategy** | **int** |  | [optional] 
**routing_meta_data** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.ip_pool_update_request import IPPoolUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IPPoolUpdateRequest from a JSON string
ip_pool_update_request_instance = IPPoolUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(IPPoolUpdateRequest.to_json())

# convert the object into a dict
ip_pool_update_request_dict = ip_pool_update_request_instance.to_dict()
# create an instance of IPPoolUpdateRequest from a dict
ip_pool_update_request_from_dict = IPPoolUpdateRequest.from_dict(ip_pool_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


