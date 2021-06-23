# TrackingEventBase

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **string** | Event type [Picked Up, Delivered, Non-Delivery, Label Created, Permission to Leave, Status] | [optional] 
**event_description** | [****](.md) | Event description and description on scanner | [optional] 
**event_description_detail** | **string** | Event description detail and description on web | [optional] 
**created_on** | [**\DateTime**](\DateTime.md) | Event date and time | [optional] 
**created_by** | **string** | Creator type | [optional] 
**lat** | **float** | Location coordinates | [optional] 
**lon** | **float** | Location coordinates | [optional] 
**carrier_name** | **string** | Carrier Name | [optional] 
**branch_code** | **string** | Branch Code | [optional] 
**run_number** | **string** | Courier Run | [optional] 
**attachments** | [**\Swagger\Client\Model\TrackingEventAttachment[]**](TrackingEventAttachment.md) | Additional scan information | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

