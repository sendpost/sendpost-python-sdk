# EIP


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_ip** | **str** | list of IP resources which are a part of the IP Pool containing public IP information. Note that the IPs specified in the IPPool should have been allocated in advance for your account | 

## Example

```python
from sendpost_python_sdk.models.eip import EIP

# TODO update the JSON string below
json = "{}"
# create an instance of EIP from a JSON string
eip_instance = EIP.from_json(json)
# print the JSON string representation of the object
print(EIP.to_json())

# convert the object into a dict
eip_dict = eip_instance.to_dict()
# create an instance of EIP from a dict
eip_from_dict = EIP.from_dict(eip_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


