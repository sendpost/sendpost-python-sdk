# Message


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | **str** | Unique ID for the message. | [optional] 
**account_id** | **int** | Account ID associated with the message. | [optional] 
**sub_account_id** | **int** | Sub-account ID associated with the message. | [optional] 
**ip_id** | **int** | IP ID used for sending the message. | [optional] 
**account_ip_pool_id** | **int** | Account IP Pool ID associated with the message. | [optional] 
**public_ip** | **str** | Public IP address used for sending the message. | [optional] 
**local_ip** | **str** | Local IP address used for sending the message. | [optional] 
**email_type** | **str** | Type of email service used. | [optional] 
**submitted_at** | **int** | UNIX epoch nano timestamp when message was submitted. | [optional] 
**var_from** | [**Person**](.md) | Object comprising name and email address of the sender | [optional] 
**reply_to** | [**Person**](.md) | Object comprising name and email addresses to which email replies will go to | [optional] 
**to** | [**MessageTo**](MessageTo.md) |  | [optional] 
**header_to** | [**MessageHeaderTo**](MessageHeaderTo.md) |  | [optional] 
**header_cc** | **List[str]** | List of CC recipients from email headers | [optional] 
**header_bcc** | **List[str]** | List of BCC recipients from email headers | [optional] 
**attachments** | **List[str]** | List of attachments | [optional] 
**groups** | **List[str]** | List of groups associated with the message | [optional] 
**ip_pool** | **str** | IP Pool from which emails will go out. Relevant only for customers on dedicated IP plans. | [optional] 
**headers** | **Dict[str, str]** | Key-Value pair which are added to every email message being sent and also with webhooks triggered on events such as email delivered, open, click etc. They are useful to identify email, recipient etc. in your internal system | [optional] 
**custom_fields** | **Dict[str, str]** | Key-Value pair of custom fields at message level | [optional] 
**subject** | **str** | Email subject line. | [optional] 
**pre_text** | **str** | Text which appears on mobile right after email subject line. | [optional] 
**html_body** | **str** | HTML email content. | [optional] 
**text_body** | **str** | Text email content. | [optional] 
**amp_body** | **str** | AMP email content. | [optional] 
**track_opens** | **bool** | Indicates if email opens need to be tracked. | [optional] 
**track_clicks** | **bool** | Indicates if email clicks need to be tracked. | [optional] 
**attempt** | **int** | Number of delivery attempts made for the message. | [optional] 
**webhook_endpoint** | **str** | Webhook endpoint URL for the message. | [optional] 
**mx_records** | **List[str]** | List of MX records for the recipient domain | [optional] 

## Example

```python
from sendpost-python-sdk.models.message import Message

# TODO update the JSON string below
json = "{}"
# create an instance of Message from a JSON string
message_instance = Message.from_json(json)
# print the JSON string representation of the object
print(Message.to_json())

# convert the object into a dict
message_dict = message_instance.to_dict()
# create an instance of Message from a dict
message_from_dict = Message.from_dict(message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


