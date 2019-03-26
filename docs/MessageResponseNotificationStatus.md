# MessageResponseNotificationStatus

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** | The status of a notification (one for each channel). \&quot;SENT\&quot;: the notification was succesfully sent to the channel (ie. email or push notification) \&quot;THROTTLED\&quot;: a temporary failure caused a retry during the notification processing;   the notification associated with this channel will be delayed for a maximum of 7 days or until the message expires \&quot;EXPIRED\&quot;: the message expired before the notification could be sent;   this means that the maximum message time to live was reached; no notification will be sent to this channel \&quot;FAILED\&quot;: a permanent failure caused the process to exit with an error, no notification will be sent to this channel | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

