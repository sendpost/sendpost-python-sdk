# Event


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_id** | **str** |  | [optional] 
**groups** | **List[str]** |  | [optional] 
**ip_id** | **int** |  | [optional] 
**ip_pool_id** | **int** |  | [optional] 
**domain_id** | **int** |  | [optional] 
**tpsp_id** | **int** |  | [optional] 
**message_type** | **str** |  | [optional] 
**message_subject** | **str** |  | [optional] 
**account_id** | **int** |  | [optional] 
**sub_account_id** | **int** |  | [optional] 
**message_id** | **str** |  | [optional] 
**type** | **int** |  | [optional] 
**var_from** | **str** |  | [optional] 
**from_name** | **str** |  | [optional] 
**to** | **str** |  | [optional] 
**to_name** | **str** |  | [optional] 
**submitted_at** | **int** |  | [optional] 
**smtp_code** | **int** |  | [optional] 
**smtp_description** | **str** |  | [optional] 
**event_metadata** | [**EventMetadata**](EventMetadata.md) |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.event import Event

# TODO update the JSON string below
json = "{}"
# create an instance of Event from a JSON string
event_instance = Event.from_json(json)
# print the JSON string representation of the object
print(Event.to_json())

# convert the object into a dict
event_dict = event_instance.to_dict()
# create an instance of Event from a dict
event_from_dict = Event.from_dict(event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


