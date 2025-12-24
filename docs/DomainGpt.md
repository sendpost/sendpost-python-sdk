# DomainGpt

GPT record host, type and value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.domain_gpt import DomainGpt

# TODO update the JSON string below
json = "{}"
# create an instance of DomainGpt from a JSON string
domain_gpt_instance = DomainGpt.from_json(json)
# print the JSON string representation of the object
print(DomainGpt.to_json())

# convert the object into a dict
domain_gpt_dict = domain_gpt_instance.to_dict()
# create an instance of DomainGpt from a dict
domain_gpt_from_dict = DomainGpt.from_dict(domain_gpt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


