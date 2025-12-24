# IPPool


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**created** | **int** |  | [optional] 
**ips** | [**List[IP]**](IP.md) |  | [optional] 
**third_party_sending_providers** | [**List[ThirdPartySendingProvider]**](ThirdPartySendingProvider.md) |  | [optional] 
**routing_strategy** | **int** |  | [optional] 
**routing_meta_data** | **str** |  | [optional] 
**auto_warmup_enabled** | **bool** |  | [optional] 
**infra_monitor** | **bool** |  | [optional] 
**ip_domain_warmup_status** | **str** |  | [optional] 
**should_overflow** | **bool** | Indicates whether the IP should overflow, once email capacity of the IP Pool has been reached, should we send remaining emails over shared IP or not | [optional] 
**overflow_pool_name** | **str** | The name of the overflow pool | [optional] 
**warmup_interval** | **int** | The interval for the warmup | [optional] 

## Example

```python
from sendpost-python-sdk.models.ip_pool import IPPool

# TODO update the JSON string below
json = "{}"
# create an instance of IPPool from a JSON string
ip_pool_instance = IPPool.from_json(json)
# print the JSON string representation of the object
print(IPPool.to_json())

# convert the object into a dict
ip_pool_dict = ip_pool_instance.to_dict()
# create an instance of IPPool from a dict
ip_pool_from_dict = IPPool.from_dict(ip_pool_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


