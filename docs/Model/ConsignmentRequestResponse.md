# ConsignmentRequestResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warnings** | **string[]** | Warnings which were encountered during processing | [optional] 
**consignment_id** | **string** | Consignment Id | [optional] 
**calculated_charge_excluding_gst** | **float** | Calculated charge excluding GST | [optional] 
**gst** | **float** | Calculated GST | [optional] 
**calculated_charge_including_gst** | **float** | Calculated charge including GST | [optional] 
**customer_references** | [**\Swagger\Client\Model\CustomerReferences**](CustomerReferences.md) |  | [optional] 
**items** | [**\Swagger\Client\Model\ConsignmentItemRequestResponse[]**](ConsignmentItemRequestResponse.md) | Consignment Items | [optional] 
**label** | [**\Swagger\Client\Model\ConsignmentLabel**](ConsignmentLabel.md) |  | [optional] 
**saturday_delivery** | **bool** | Defines whether saturday delivery has been accepted | [optional] 
**no_split_delivery** | **bool** | Defines whether no-split delivery has been accepted | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

