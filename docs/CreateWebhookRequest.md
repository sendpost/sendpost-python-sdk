# CreateWebhookRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Is the webhook active or in a paused state? | [optional] 
**url** | **str** | URL endpoint to which webhook calls are sent. | [optional] 
**processed** | **bool** | Trigger webhook on email message being processed. | [optional] 
**delivered** | **bool** | Trigger webhook on email message being delivered. | [optional] 
**dropped** | **bool** | Trigger webhook on email message being dropped. | [optional] 
**soft_bounced** | **bool** | Trigger webhook on email message being soft bounced. | [optional] 
**hard_bounced** | **bool** | Trigger webhook on email message being hard bounced. | [optional] 
**opened** | **bool** | Trigger webhook on email message being opened. | [optional] 
**clicked** | **bool** | Trigger webhook on email message link being clicked. | [optional] 
**unsubscribed** | **bool** | Trigger webhook on email message being unsubscribed. | [optional] 
**spam** | **bool** | Trigger webhook on email message being marked as spam. | [optional] 
**sent** | **bool** | Trigger webhook on email message being sent. | [optional] 
**smtp_dropped** | **bool** | Trigger webhook on email message being dropped by SMTP. | [optional] 
**unique_open** | **bool** | Trigger webhook on unique email opens. | [optional] 
**unique_click** | **bool** | Trigger webhook on unique email clicks. | [optional] 

## Example

```python
from sendpost-python-sdk.models.create_webhook_request import CreateWebhookRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWebhookRequest from a JSON string
create_webhook_request_instance = CreateWebhookRequest.from_json(json)
# print the JSON string representation of the object
print(CreateWebhookRequest.to_json())

# convert the object into a dict
create_webhook_request_dict = create_webhook_request_instance.to_dict()
# create an instance of CreateWebhookRequest from a dict
create_webhook_request_from_dict = CreateWebhookRequest.from_dict(create_webhook_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


