# DomainDmarc

DMARC record host, type and value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.domain_dmarc import DomainDmarc

# TODO update the JSON string below
json = "{}"
# create an instance of DomainDmarc from a JSON string
domain_dmarc_instance = DomainDmarc.from_json(json)
# print the JSON string representation of the object
print(DomainDmarc.to_json())

# convert the object into a dict
domain_dmarc_dict = domain_dmarc_instance.to_dict()
# create an instance of DomainDmarc from a dict
domain_dmarc_from_dict = DomainDmarc.from_dict(domain_dmarc_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


