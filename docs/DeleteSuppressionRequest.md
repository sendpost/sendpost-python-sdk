# DeleteSuppressionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**suppressions** | [**List[CreateSuppressionRequestSpamComplaintInner]**](CreateSuppressionRequestSpamComplaintInner.md) |  | [optional] 

## Example

```python
from sendpost_python_sdk.models.delete_suppression_request import DeleteSuppressionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteSuppressionRequest from a JSON string
delete_suppression_request_instance = DeleteSuppressionRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteSuppressionRequest.to_json())

# convert the object into a dict
delete_suppression_request_dict = delete_suppression_request_instance.to_dict()
# create an instance of DeleteSuppressionRequest from a dict
delete_suppression_request_from_dict = DeleteSuppressionRequest.from_dict(delete_suppression_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


