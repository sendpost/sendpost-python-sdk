# WebhookObject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | [**Event**](Event.md) |  | [optional] 
**email_message** | [**EmailMessage**](EmailMessage.md) |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.webhook_object import WebhookObject

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookObject from a JSON string
webhook_object_instance = WebhookObject.from_json(json)
# print the JSON string representation of the object
print(WebhookObject.to_json())

# convert the object into a dict
webhook_object_dict = webhook_object_instance.to_dict()
# create an instance of WebhookObject from a dict
webhook_object_from_dict = WebhookObject.from_dict(webhook_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


