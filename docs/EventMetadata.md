# EventMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**smtp_code** | **int** |  | [optional] 
**smtp_description** | **str** |  | [optional] 
**user_agent** | [**UserAgent**](UserAgent.md) |  | [optional] 
**os** | [**OperatingSystem**](OperatingSystem.md) |  | [optional] 
**device** | [**Device**](Device.md) |  | [optional] 
**geo** | [**GeoLocation**](GeoLocation.md) |  | [optional] 
**clicked_url** | **str** |  | [optional] 
**tracked_ip** | **str** |  | [optional] 
**raw_user_agent** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.event_metadata import EventMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of EventMetadata from a JSON string
event_metadata_instance = EventMetadata.from_json(json)
# print the JSON string representation of the object
print(EventMetadata.to_json())

# convert the object into a dict
event_metadata_dict = event_metadata_instance.to_dict()
# create an instance of EventMetadata from a dict
event_metadata_from_dict = EventMetadata.from_dict(event_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


