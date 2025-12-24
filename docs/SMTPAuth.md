# SMTPAuth


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the SMTP Auth | [optional] 
**username** | **str** | Username for the SMTP Auth | [optional] 
**password** | **str** | Password for the SMTP Auth | [optional] 
**created** | **int** | UNIX epoch nano timestamp when the SMTP Auth was created | [optional] 
**updated** | **int** | UNIX epoch nano timestamp when the SMTP Auth was updated | [optional] 

## Example

```python
from sendpost-python-sdk.models.smtp_auth import SMTPAuth

# TODO update the JSON string below
json = "{}"
# create an instance of SMTPAuth from a JSON string
smtp_auth_instance = SMTPAuth.from_json(json)
# print the JSON string representation of the object
print(SMTPAuth.to_json())

# convert the object into a dict
smtp_auth_dict = smtp_auth_instance.to_dict()
# create an instance of SMTPAuth from a dict
smtp_auth_from_dict = SMTPAuth.from_dict(smtp_auth_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


