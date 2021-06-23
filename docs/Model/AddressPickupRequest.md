# AddressPickupRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contact** | **string** | Sender contact details | [optional] 
**contact_phone_number** | **string** | Phone number of the contact. | [optional] 
**address** | [**\Swagger\Client\Model\Address**](Address.md) |  | 
**pickup_from_time** | [**\DateTime**](\DateTime.md) | The open window for pickup | [optional] 
**instructions** | **string** | Any courier instructions required for this pickup | [optional] 
**service_standard** | **string** | The service is applied to the consignment | [optional] 
**items** | [**\Swagger\Client\Model\Item[]**](Item.md) | a list of items to be picked up | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

