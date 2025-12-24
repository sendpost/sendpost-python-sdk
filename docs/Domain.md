# Domain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the domain. | [optional] 
**name** | **str** | Name of the domain. | [optional] 
**dkim** | [**DomainDkim**](DomainDkim.md) |  | [optional] 
**return_path** | [**DomainReturnPath**](DomainReturnPath.md) |  | [optional] 
**track** | [**DomainTrack**](DomainTrack.md) |  | [optional] 
**dmarc** | [**DomainDmarc**](DomainDmarc.md) |  | [optional] 
**dkim_config** | **str** | DKIM configuration | [optional] 
**dkim_verified** | **bool** | Status of DKIM verification ( true or false ) | [optional] 
**dmarc_verified** | **bool** | Status of DMARC verification ( true or false) | [optional] 
**return_path_verified** | **bool** | Status of ReturnPath verification ( true or false ) | [optional] 
**track_verified** | **bool** | Status of Track verification ( true or false ) | [optional] 
**verified** | **bool** | Overall verification status of the domain | [optional] 
**domain_registered_date** | **str** | Date when the domain was registered | [optional] 
**created** | **int** | UNIX epoch timestamp in nanoseconds. | [optional] 
**gpt_verified** | **bool** | Status of GPT verification ( true or false ) | [optional] 
**gpt** | [**DomainGpt**](DomainGpt.md) |  | [optional] 
**dmarc_failure_reason** | **str** | Reason for DMARC verification failure | [optional] 
**dkim_failure_reason** | **str** | Reason for DKIM verification failure | [optional] 
**track_failure_reason** | **str** | Reason for Track verification failure | [optional] 
**return_path_failure_reason** | **str** | Reason for ReturnPath verification failure | [optional] 

## Example

```python
from sendpost_python_sdk.models.domain import Domain

# TODO update the JSON string below
json = "{}"
# create an instance of Domain from a JSON string
domain_instance = Domain.from_json(json)
# print the JSON string representation of the object
print(Domain.to_json())

# convert the object into a dict
domain_dict = domain_instance.to_dict()
# create an instance of Domain from a dict
domain_from_dict = Domain.from_dict(domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


