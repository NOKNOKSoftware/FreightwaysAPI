# Consignment

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**consignment_id** | **string** | Unique consignment identifier | [optional] 
**consignment_reference** | **string** | Defines the customers number for this consignment | [optional] 
**consignment_date** | [**\DateTime**](\DateTime.md) | Date in Utc when consignment record was created | [optional] 
**created_date_time** | [**\DateTime**](\DateTime.md) | Date in Utc when consignment record was created | [optional] 
**sequence_id** | **int** | Used when customer operate multiple sites repeaing consignment numbers. | [optional] 
**status** | **string** | Consignment Status | [optional] 
**pickup_rate_zone** | **string** | Rating Zone of the Pickup | [optional] 
**delivery_rate_zone** | **string** | Rating Zone of the Delivery | [optional] 
**signature_required** | **bool** | Defines either signature is required or not | [optional] 
**saturday_delivery** | **bool** | Defines either saturday delivery is required or not | [optional] 
**no_split_delivery** | **bool** | Defines either no-split delivery is required or not | [optional] 
**calculated_charge_excluding_gst** | **float** | Calculated charge excluding GST | [optional] 
**gst** | **float** | Calculated GST | [optional] 
**calculated_charge_including_gst** | **float** | Calculated charge including GST | [optional] 
**notifications** | [**\Swagger\Client\Model\Notifications**](Notifications.md) |  | [optional] 
**sender** | [**\Swagger\Client\Model\Sender**](Sender.md) |  | [optional] 
**receiver** | [**\Swagger\Client\Model\Receiver**](Receiver.md) |  | [optional] 
**customer_references** | [**\Swagger\Client\Model\CustomerReferences**](CustomerReferences.md) |  | [optional] 
**label** | [**\Swagger\Client\Model\ConsignmentLabel**](ConsignmentLabel.md) |  | [optional] 
**items** | [**\Swagger\Client\Model\ConsignmentItem[]**](ConsignmentItem.md) | Defines the set of the consignments | [optional] 
**cancellation_request** | [**\Swagger\Client\Model\CancellationRequestItem**](CancellationRequestItem.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

