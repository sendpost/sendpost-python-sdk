# DomainTrack

Track record host, type and value. This domain will be used for link tracking while rewriting links in your email message

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**text_value** | **str** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.domain_track import DomainTrack

# TODO update the JSON string below
json = "{}"
# create an instance of DomainTrack from a JSON string
domain_track_instance = DomainTrack.from_json(json)
# print the JSON string representation of the object
print(DomainTrack.to_json())

# convert the object into a dict
domain_track_dict = domain_track_instance.to_dict()
# create an instance of DomainTrack from a dict
domain_track_from_dict = DomainTrack.from_dict(domain_track_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


