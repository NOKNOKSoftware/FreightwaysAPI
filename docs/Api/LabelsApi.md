# Swagger\Client\LabelsApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getLabelByConsignmentId**](LabelsApi.md#getlabelbyconsignmentid) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/labels | Consignment by Id.

# **getLabelByConsignmentId**
> string getLabelByConsignmentId($carrier_name, $customer_id, $consignment_id, $format, $size)

Consignment by Id.

Get consignment data from the Freightways system by ConsignmentId

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LabelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_id = "consignment_id_example"; // string | The consignment identifier
$format = "format_example"; // string | Required format of the label - PDF
$size = "size_example"; // string | Required size of the label - A4, FreThermal, FreThermal-120x110, FreThermal-174x100. Note: FreThermal is an alias for FreThermal-120x110

try {
    $result = $apiInstance->getLabelByConsignmentId($carrier_name, $customer_id, $consignment_id, $format, $size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LabelsApi->getLabelByConsignmentId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_id** | **string**| The consignment identifier |
 **format** | **string**| Required format of the label - PDF |
 **size** | **string**| Required size of the label - A4, FreThermal, FreThermal-120x110, FreThermal-174x100. Note: FreThermal is an alias for FreThermal-120x110 |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

