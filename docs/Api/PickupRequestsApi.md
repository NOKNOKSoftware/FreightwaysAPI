# Swagger\Client\PickupRequestsApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPickupRequest**](PickupRequestsApi.md#createpickuprequest) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/pickup-requests/pickup-location | Lodge a pickup request for the Carrier (carrierName) and customer (customerId) at the provided PickupLocationId
[**createPickupRequestByGeo**](PickupRequestsApi.md#createpickuprequestbygeo) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/pickup-requests/address | PickupRequest the pickup request based on an address

# **createPickupRequest**
> \Swagger\Client\Model\PickupRequestDetails createPickupRequest($carrier_name, $customer_id, $body)

Lodge a pickup request for the Carrier (carrierName) and customer (customerId) at the provided PickupLocationId

Lodge a pickup request for the Carrier (carrierName) and customer (customerId) at the provided PickupLocationId

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PickupRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$body = new \Swagger\Client\Model\PickupLocationPickupRequest(); // \Swagger\Client\Model\PickupLocationPickupRequest | PickupRequest pickup details

try {
    $result = $apiInstance->createPickupRequest($carrier_name, $customer_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PickupRequestsApi->createPickupRequest: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **body** | [**\Swagger\Client\Model\PickupLocationPickupRequest**](../Model/PickupLocationPickupRequest.md)| PickupRequest pickup details | [optional]

### Return type

[**\Swagger\Client\Model\PickupRequestDetails**](../Model/PickupRequestDetails.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createPickupRequestByGeo**
> \Swagger\Client\Model\PickupRequestDetails createPickupRequestByGeo($carrier_name, $customer_id, $body)

PickupRequest the pickup request based on an address

PickupRequest the pickup request based on an address.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PickupRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Freightways Carrier Customer Id
$body = new \Swagger\Client\Model\AddressPickupRequest(); // \Swagger\Client\Model\AddressPickupRequest | Pickup Request details with geo coordinate

try {
    $result = $apiInstance->createPickupRequestByGeo($carrier_name, $customer_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PickupRequestsApi->createPickupRequestByGeo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Freightways Carrier Customer Id |
 **body** | [**\Swagger\Client\Model\AddressPickupRequest**](../Model/AddressPickupRequest.md)| Pickup Request details with geo coordinate | [optional]

### Return type

[**\Swagger\Client\Model\PickupRequestDetails**](../Model/PickupRequestDetails.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

