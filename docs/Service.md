# Service

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authorized_cidrs** | **list[str]** | Allowed source IPs or CIDRs for this service. | 
**authorized_recipients** | **list[str]** | If non empty, the service will be able to send messages only to these fiscal codes. | 
**department_name** | **str** | The department inside the organization that runs the service. Will be added to the content of sent messages. | 
**id** | **str** |  | [optional] 
**is_visible** | **bool** |  | [optional] [default to False]
**max_allowed_payment_amount** | **int** | Maximum amount in euro cents that a service is allowed to charge to a user. | [optional] 
**organization_fiscal_code** | **str** | Organization fiscal code. | 
**organization_name** | **str** | The organization that runs the service. Will be added to the content of sent messages to identify the sender. | 
**service_id** | **str** | The ID of the Service. Equals the subscriptionId of a registered API user. | 
**service_name** | **str** | The name of the service. Will be added to the content of sent messages. | 
**version** | **int** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

