# Suppression


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | The ID of the suppression | [optional] 
**reason** | **int** | The reason for the suppression (0 &#x3D; manual, 1 &#x3D; unsubscribe, 2 &#x3D; hard bounce, 3 &#x3D; spam complaint) | [optional] 
**smtp_error** | **str** | SMTP error code in case of hard bounce suppression | [optional] 
**email** | **str** | The email address for the suppression | [optional] 
**created** | **int** | UNIX epoch nano timestamp when the suppression was created | [optional] 

## Example

```python
from sendpost-python-sdk.models.suppression import Suppression

# TODO update the JSON string below
json = "{}"
# create an instance of Suppression from a JSON string
suppression_instance = Suppression.from_json(json)
# print the JSON string representation of the object
print(Suppression.to_json())

# convert the object into a dict
suppression_dict = suppression_instance.to_dict()
# create an instance of Suppression from a dict
suppression_from_dict = Suppression.from_dict(suppression_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


