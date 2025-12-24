# AutoWarmupPlan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the auto-warmup plan | [optional] 
**name** | **str** | Name of the auto-warmup plan | [optional] 
**gmail_warmup_plan** | **str** | Gmail warmup plan configuration in JSON format | [optional] 
**yahoo_warmup_plan** | **str** | Yahoo warmup plan configuration in JSON format | [optional] 
**aol_warmup_plan** | **str** | AOL warmup plan configuration in JSON format | [optional] 
**microsoft_warmup_plan** | **str** | Microsoft warmup plan configuration in JSON format | [optional] 
**comcast_warmup_plan** | **str** | Comcast warmup plan configuration in JSON format | [optional] 
**yandex_warmup_plan** | **str** | Yandex warmup plan configuration in JSON format | [optional] 
**gmx_warmup_plan** | **str** | GMX warmup plan configuration in JSON format | [optional] 
**mailru_warmup_plan** | **str** | Mail.ru warmup plan configuration in JSON format | [optional] 
**icloud_warmup_plan** | **str** | iCloud warmup plan configuration in JSON format | [optional] 
**zoho_warmup_plan** | **str** | Zoho warmup plan configuration in JSON format | [optional] 
**qq_warmup_plan** | **str** | QQ warmup plan configuration in JSON format | [optional] 
**default_warmup_plan** | **str** | Default warmup plan configuration in JSON format | [optional] 
**att_warmup_plan** | **str** | AT&amp;T warmup plan configuration in JSON format | [optional] 
**office365_warmup_plan** | **str** | Office365 warmup plan configuration in JSON format | [optional] 
**googleworkspace_warmup_plan** | **str** | Google Workspace warmup plan configuration in JSON format | [optional] 
**proofpoint_warmup_plan** | **str** | Proofpoint warmup plan configuration in JSON format | [optional] 
**mimecast_warmup_plan** | **str** | Mimecast warmup plan configuration in JSON format | [optional] 
**barracuda_warmup_plan** | **str** | Barracuda warmup plan configuration in JSON format | [optional] 
**ciscoironport_warmup_plan** | **str** | Cisco IronPort warmup plan configuration in JSON format | [optional] 
**rackspace_warmup_plan** | **str** | Rackspace warmup plan configuration in JSON format | [optional] 
**zohobusiness_warmup_plan** | **str** | Zoho Business warmup plan configuration in JSON format | [optional] 
**amazonworkmail_warmup_plan** | **str** | Amazon WorkMail warmup plan configuration in JSON format | [optional] 
**symantec_warmup_plan** | **str** | Symantec warmup plan configuration in JSON format | [optional] 
**fortinet_warmup_plan** | **str** | Fortinet warmup plan configuration in JSON format | [optional] 
**sophos_warmup_plan** | **str** | Sophos warmup plan configuration in JSON format | [optional] 
**trendmicro_warmup_plan** | **str** | Trend Micro warmup plan configuration in JSON format | [optional] 
**checkpoint_warmup_plan** | **str** | Checkpoint warmup plan configuration in JSON format | [optional] 
**created** | **int** | UNIX epoch nano timestamp when the warmup plan was created | [optional] 
**updated** | **int** | UNIX epoch nano timestamp when the warmup plan was last updated | [optional] 
**warmup_interval** | **int** | Warmup interval in hours | [optional] 

## Example

```python
from sendpost-python-sdk.models.auto_warmup_plan import AutoWarmupPlan

# TODO update the JSON string below
json = "{}"
# create an instance of AutoWarmupPlan from a JSON string
auto_warmup_plan_instance = AutoWarmupPlan.from_json(json)
# print the JSON string representation of the object
print(AutoWarmupPlan.to_json())

# convert the object into a dict
auto_warmup_plan_dict = auto_warmup_plan_instance.to_dict()
# create an instance of AutoWarmupPlan from a dict
auto_warmup_plan_from_dict = AutoWarmupPlan.from_dict(auto_warmup_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


