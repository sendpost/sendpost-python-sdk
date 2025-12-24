# ThirdPartySendingProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **int** |  | [optional] 
**domain** | **str** |  | [optional] 
**endpoint** | **str** |  | [optional] 
**key** | **str** |  | [optional] 
**secret** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**oauth_token** | **str** |  | [optional] 
**retry_time** | **int** |  | [optional] 
**created** | **int** |  | [optional] 

## Example

```python
from sendpost-python-sdk.models.third_party_sending_provider import ThirdPartySendingProvider

# TODO update the JSON string below
json = "{}"
# create an instance of ThirdPartySendingProvider from a JSON string
third_party_sending_provider_instance = ThirdPartySendingProvider.from_json(json)
# print the JSON string representation of the object
print(ThirdPartySendingProvider.to_json())

# convert the object into a dict
third_party_sending_provider_dict = third_party_sending_provider_instance.to_dict()
# create an instance of ThirdPartySendingProvider from a dict
third_party_sending_provider_from_dict = ThirdPartySendingProvider.from_dict(third_party_sending_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


