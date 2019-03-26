# ExtendedProfile

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blocked_inbox_or_channels** | **dict** | All the notification channels blocked by the user. Each channel is related to a specific service (sender). | [optional] 
**email** | **str** |  | [optional] 
**is_inbox_enabled** | **bool** | True if the recipient of a message wants to store its content for later retrieval. | [default to False]
**is_webhook_enabled** | **bool** | True if the recipient of a message wants to forward the notifications to the default webhook. | [default to False]
**preferred_languages** | **list[str]** | Indicates the User&#x27;s preferred written or spoken languages in order of preference. Generally used for selecting a localized User interface. Valid values are concatenation of the ISO 639-1 two letter language code, an underscore, and the ISO 3166-1 2 letter country code; e.g., &#x27;en_US&#x27; specifies the language English and country US. | [optional] 
**version** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

