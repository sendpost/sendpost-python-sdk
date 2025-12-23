# DomainReturnPath

ReturnPath record host, type and value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.domain_return_path import DomainReturnPath

# TODO update the JSON string below
json = "{}"
# create an instance of DomainReturnPath from a JSON string
domain_return_path_instance = DomainReturnPath.from_json(json)
# print the JSON string representation of the object
print(DomainReturnPath.to_json())

# convert the object into a dict
domain_return_path_dict = domain_return_path_instance.to_dict()
# create an instance of DomainReturnPath from a dict
domain_return_path_from_dict = DomainReturnPath.from_dict(domain_return_path_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


