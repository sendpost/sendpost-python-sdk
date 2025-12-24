# CreateDomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the domain (e.g., hooli.com). | [optional] 

## Example

```python
from sendpost_python_sdk.models.create_domain_request import CreateDomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateDomainRequest from a JSON string
create_domain_request_instance = CreateDomainRequest.from_json(json)
# print the JSON string representation of the object
print(CreateDomainRequest.to_json())

# convert the object into a dict
create_domain_request_dict = create_domain_request_instance.to_dict()
# create an instance of CreateDomainRequest from a dict
create_domain_request_from_dict = CreateDomainRequest.from_dict(create_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


