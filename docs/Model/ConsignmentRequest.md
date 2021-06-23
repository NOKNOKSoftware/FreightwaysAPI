# ConsignmentRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signature_required** | **bool** | Defines either signature is required or not | [optional] 
**saturday_delivery** | **bool** | Defines either saturday delivery is required or not | [optional] 
**no_split_delivery** | **bool** | Defines either no-split delivery is required or not | [optional] 
**consignment_reference** | **string** | Defines the unique customer reference for this consignment, must be alphanumeric i.e. a-z A-Z 0-9 | 
**consignment_date** | [**\DateTime**](\DateTime.md) | Consignment date in Utc. If not provided the current date will be used. | [optional] 
**service_standard** | **string** | Service Standard (Overnight, Two Day, Same Day) for the consignment (case insensitive) | 
**sequence_id** | **int** | Used when customer operate multiple sites repeating consignment numbers. If not provided 1 will be used. | [optional] [default to 1]
**notifications** | [**\Swagger\Client\Model\Notifications**](Notifications.md) |  | [optional] 
**sender** | [**\Swagger\Client\Model\Sender**](Sender.md) |  | 
**receiver** | [**\Swagger\Client\Model\Receiver**](Receiver.md) |  | 
**customer_references** | [**\Swagger\Client\Model\CustomerReferences**](CustomerReferences.md) |  | [optional] 
**standard_items** | [**\Swagger\Client\Model\StandardItemRequest[]**](StandardItemRequest.md) | Defines standard rated items in the consignments | [optional] 
**base_plus_items** | [**\Swagger\Client\Model\BasePlusItemRequest**](BasePlusItemRequest.md) |  | [optional] 
**satchel_items** | [**\Swagger\Client\Model\SatchelItemRequest[]**](SatchelItemRequest.md) | Defines satchels included in the consignment | [optional] 
**label** | [**\Swagger\Client\Model\ConsignmentLabelRequest**](ConsignmentLabelRequest.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

