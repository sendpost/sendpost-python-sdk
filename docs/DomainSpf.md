# DomainSpf

SPF record host, type and value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.domain_spf import DomainSpf

# TODO update the JSON string below
json = "{}"
# create an instance of DomainSpf from a JSON string
domain_spf_instance = DomainSpf.from_json(json)
# print the JSON string representation of the object
print(DomainSpf.to_json())

# convert the object into a dict
domain_spf_dict = domain_spf_instance.to_dict()
# create an instance of DomainSpf from a dict
domain_spf_from_dict = DomainSpf.from_dict(domain_spf_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


