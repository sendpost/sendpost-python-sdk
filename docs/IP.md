# IP


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique ID for the IP | 
**public_ip** | **str** | The public IP address associated with the resource | 
**system_domain** | [**Domain**](.md) | Details of the system domain associated with the IP | [optional] 
**reverse_dns_hostname** | **str** | The reverse DNS hostname for the IP | [optional] 
**type** | **int** | Type of the IP | [optional] 
**gmail_settings** | **str** | Configuration for Gmail delivery settings in JSON format | [optional] 
**yahoo_settings** | **str** | Configuration for Yahoo delivery settings in JSON format | [optional] 
**aol_settings** | **str** | Configuration for AOL delivery settings in JSON format | [optional] 
**microsoft_settings** | **str** | Configuration for Microsoft delivery settings in JSON format | [optional] 
**comcast_settings** | **str** | Configuration for Comcast delivery settings in JSON format | [optional] 
**yandex_settings** | **str** | Configuration for Yandex delivery settings in JSON format | [optional] 
**gmx_settings** | **str** | Configuration for GMX delivery settings in JSON format | [optional] 
**mailru_settings** | **str** | Configuration for Mail.ru delivery settings in JSON format | [optional] 
**icloud_settings** | **str** | Configuration for iCloud delivery settings in JSON format | [optional] 
**zoho_settings** | **str** | Configuration for Zoho delivery settings in JSON format | [optional] 
**qq_settings** | **str** | Configuration for QQ delivery settings in JSON format | [optional] 
**default_settings** | **str** | Default delivery settings in JSON format | [optional] 
**att_settings** | **str** | Configuration for AT&amp;T delivery settings in JSON format | [optional] 
**created** | **int** | The timestamp (UNIX epoch) when the IP was created | 
**infra_classification** | **str** | Classification of the infrastructure | [optional] 
**infra_monitor** | **bool** | Indicates whether infrastructure monitoring is enabled | [optional] 
**state** | **int** | The state of the IP | [optional] 
**auto_warmup_plan** | **str** | The auto-warmup plan associated with the IP | [optional] 

## Example

```python
from sendpost_python_sdk.models.ip import IP

# TODO update the JSON string below
json = "{}"
# create an instance of IP from a JSON string
ip_instance = IP.from_json(json)
# print the JSON string representation of the object
print(IP.to_json())

# convert the object into a dict
ip_dict = ip_instance.to_dict()
# create an instance of IP from a dict
ip_from_dict = IP.from_dict(ip_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


