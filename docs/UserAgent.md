# UserAgent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**family** | **str** |  | [optional] 
**major** | **str** |  | [optional] 
**minor** | **str** |  | [optional] 
**patch** | **str** |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.user_agent import UserAgent

# TODO update the JSON string below
json = "{}"
# create an instance of UserAgent from a JSON string
user_agent_instance = UserAgent.from_json(json)
# print the JSON string representation of the object
print(UserAgent.to_json())

# convert the object into a dict
user_agent_dict = user_agent_instance.to_dict()
# create an instance of UserAgent from a dict
user_agent_from_dict = UserAgent.from_dict(user_agent_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


