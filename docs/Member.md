# Member


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the member | [optional] 
**is_verified** | **bool** | Indicates whether the member is verified | [optional] 
**is_forbidden** | **bool** | Indicates whether the member is forbidden | [optional] 
**firebase_uid** | **str** | Firebase UID for the member | [optional] 
**email** | **str** | Email for the member | [optional] 
**name** | **str** | Name for the member | [optional] 
**url** | **str** | Logo URL for the member | [optional] 
**company_name** | **str** | Company name for the member | [optional] 
**onboard_q_answered** | **bool** | Indicates whether the member has answered onboarding question | [optional] 
**phone_number** | **str** | Phone number for the member | [optional] 
**notes_color** | **str** | Color for the member&#39;s notes | [optional] 
**created** | **int** | UNIX epoch nano timestamp when the member was created | [optional] 

## Example

```python
from sendpost_python_sdk.models.member import Member

# TODO update the JSON string below
json = "{}"
# create an instance of Member from a JSON string
member_instance = Member.from_json(json)
# print the JSON string representation of the object
print(Member.to_json())

# convert the object into a dict
member_dict = member_instance.to_dict()
# create an instance of Member from a dict
member_from_dict = Member.from_dict(member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


