# ConsignmentItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**consignment_item_id** | **string** | Unique Consignment Item Id | [optional] 
**item_reference** | **string** | customer specified item reference | [optional] 
**rate_service_code** | **string** | Rating code for the consignment item | [optional] 
**satchel_type** | **string** | Satchel product type e.g. E20 | [optional] 
**weight** | **float** | Consignment weight | [optional] 
**volume** | **float** | Consignment volume | [optional] 
**barcode** | **string** | Consignment Item barcode | [optional] 
**status** | **string** | Consignment Item Status | [optional] 
**pickup_date_time** | [**\DateTime**](\DateTime.md) | Timestamp of Pickup in Utc | [optional] 
**onboard_date_time** | [**\DateTime**](\DateTime.md) | Timestamp of Onboard in Utc | [optional] 
**delivery_date_time** | [**\DateTime**](\DateTime.md) | Timestamp of Delivery | [optional] 
**total_rate_breakdown** | [**\Swagger\Client\Model\BreakdownComponent[]**](BreakdownComponent.md) | breakdown to the total cost of this consignment item | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

