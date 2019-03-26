# MessageContent

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**due_date** | **str** | A date-time field in ISO-8601 format and UTC timezone. | [optional] 
**markdown** | **str** | The full version of the message, in plain text or Markdown format. The content of this field will be delivered to channels that don&#x27;t have any limit in terms of content size (e.g. email, etc...). | 
**payment_data** | [**MessageContentPaymentData**](MessageContentPaymentData.md) |  | [optional] 
**subject** | **str** | The (optional) subject of the message - note that only some notification channels support the display of a subject. When a subject is not provided, one gets generated from the client attributes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

