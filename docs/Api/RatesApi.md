# Swagger\Client\RatesApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStandardRates**](RatesApi.md#getstandardrates) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/rates | Finds rates using the standard Weight or Volume model for a given query

# **getStandardRates**
> \Swagger\Client\Model\Rate[] getStandardRates($carrier_name, $customer_id, $body)

Finds rates using the standard Weight or Volume model for a given query

Fetch rates for a consignment being sent from one point to another. For example; get a rate for sending an item of 0.015 m3 from an Auckland location to a Wellington location using an overnight service with signature required. Multiple rates may be returned from depending on the configuration of the account associated with the customer provided.  This includes returning rates from other carriers if the customer has accounts connected with other carriers.</br></br> **NOTE:** For customers with multiple carriers it is important that when posting a consignment the carrier and customer id matching the desired rate is used.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\RatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Freightways Carrier Customer Id
$body = new \Swagger\Client\Model\RatesRequest(); // \Swagger\Client\Model\RatesRequest | Consignment data that needs to be rated

try {
    $result = $apiInstance->getStandardRates($carrier_name, $customer_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RatesApi->getStandardRates: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Freightways Carrier Customer Id |
 **body** | [**\Swagger\Client\Model\RatesRequest**](../Model/RatesRequest.md)| Consignment data that needs to be rated | [optional]

### Return type

[**\Swagger\Client\Model\Rate[]**](../Model/Rate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

