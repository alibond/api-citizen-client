# MessageResponseWithContent

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | [**MessageResponseWithContentMessage**](MessageResponseWithContentMessage.md) |  | 
**notification** | [**MessageResponseWithoutContentNotification**](MessageResponseWithoutContentNotification.md) |  | [optional] 
**status** | **str** | The processing status of a message. \&quot;ACCEPTED\&quot;: the message has been accepted and will be processed for delivery;   we&#x27;ll try to store its content in the user&#x27;s inbox and notify him on his preferred channels \&quot;THROTTLED\&quot;: a temporary failure caused a retry during the message processing;   any notification associated with this message will be delayed for a maximum of 7 days \&quot;FAILED\&quot;: a permanent failure caused the process to exit with an error, no notification will be sent for this message \&quot;PROCESSED\&quot;: the message was succesfully processed and is now stored in the user&#x27;s inbox;   we&#x27;ll try to send a notification for each of the selected channels | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

