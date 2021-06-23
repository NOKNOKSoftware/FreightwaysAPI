# RatesRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pickup_address** | [**\Swagger\Client\Model\Address**](Address.md) |  | [optional] 
**delivery_address** | [**\Swagger\Client\Model\Address**](Address.md) |  | [optional] 
**signature_required** | **bool** | Defines either signature is required or not | [optional] 
**saturday_delivery** | **bool** | Defines either saturday delivery is required or not | [optional] 
**txt_notification** | **bool** | Defines either text notification is required or not | [optional] 
**service_standard** | **string** |  | [optional] 
**standard_items** | [**\Swagger\Client\Model\StandardItemRateRequest[]**](StandardItemRateRequest.md) | List of standard items within the consignment to rate | [optional] 
**base_plus_items** | [**\Swagger\Client\Model\BasePlusItemRateRequest**](BasePlusItemRateRequest.md) |  | [optional] 
**satchel_items** | [**\Swagger\Client\Model\SatchelItemRateRequest[]**](SatchelItemRateRequest.md) | List of base plus items within the consignment to rate | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

