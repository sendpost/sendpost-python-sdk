# DomainDkim

DKIM record host, type and value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.domain_dkim import DomainDkim

# TODO update the JSON string below
json = "{}"
# create an instance of DomainDkim from a JSON string
domain_dkim_instance = DomainDkim.from_json(json)
# print the JSON string representation of the object
print(DomainDkim.to_json())

# convert the object into a dict
domain_dkim_dict = domain_dkim_instance.to_dict()
# create an instance of DomainDkim from a dict
domain_dkim_from_dict = DomainDkim.from_dict(domain_dkim_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


