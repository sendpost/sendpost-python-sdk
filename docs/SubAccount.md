# SubAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the sub-account. | [optional] 
**api_key** | **str** | API key for the sub-account. | [optional] 
**name** | **str** | Name of the sub-account. | [optional] 
**labels** | [**List[Label]**](Label.md) | Labels associated with the sub-account | [optional] 
**smtp_auths** | [**List[SMTPAuth]**](SMTPAuth.md) | SMTP Auths associated with the sub-account | [optional] 
**type** | **int** | Type of the sub-account | [optional] 
**is_plus** | **bool** | Indicates whether the sub-account is a Plus sub-account | [optional] 
**created** | **int** | UNIX epoch nano timestamp when the sub-account was created. | [optional] 
**created_by** | **Dict[str, object]** | Member who created the sub-account | [optional] 
**updated_by** | **Dict[str, object]** | Member who updated the sub-account | [optional] 
**blocked** | **bool** | Indicates whether the sub-account is blocked | [optional] 
**blocked_at** | **int** | UNIX epoch nano timestamp when the sub-account was blocked (0 if not blocked) | [optional] 
**block_reason** | **str** | Reason for blocking the sub-account | [optional] 
**hb_exempt** | **bool** | Indicates whether the sub-account is exempt from hard bounce tracking | [optional] 
**generate_weekly_report** | **bool** | Indicates whether weekly reports are generated for this sub-account | [optional] 
**handlers** | **List[str]** | Handlers associated with the sub-account | [optional] 

## Example

```python
from sendpost-python-sdk.models.sub_account import SubAccount

# TODO update the JSON string below
json = "{}"
# create an instance of SubAccount from a JSON string
sub_account_instance = SubAccount.from_json(json)
# print the JSON string representation of the object
print(SubAccount.to_json())

# convert the object into a dict
sub_account_dict = sub_account_instance.to_dict()
# create an instance of SubAccount from a dict
sub_account_from_dict = SubAccount.from_dict(sub_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


