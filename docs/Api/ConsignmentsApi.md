# Swagger\Client\ConsignmentsApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelConsignmentById**](ConsignmentsApi.md#cancelconsignmentbyid) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/cancellationrequests | Request cancellation of a Consignment by Id.
[**getConsignmentById**](ConsignmentsApi.md#getconsignmentbyid) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId} | Consignment by Id.
[**getConsignmentsByParameters**](ConsignmentsApi.md#getconsignmentsbyparameters) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments | Search consignments based on Consignment / Sender / Receiver details
[**postConsignment**](ConsignmentsApi.md#postconsignment) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/consignments | Upload consignment data.

# **cancelConsignmentById**
> string cancelConsignmentById($carrier_name, $customer_id, $consignment_id, $body)

Request cancellation of a Consignment by Id.

Lodges a request to cancel a consignment.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ConsignmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_id = "consignment_id_example"; // string | The consignment identifier
$body = new \Swagger\Client\Model\CancellationRequest(); // \Swagger\Client\Model\CancellationRequest | Consignment data that needs to be stored

try {
    $result = $apiInstance->cancelConsignmentById($carrier_name, $customer_id, $consignment_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsignmentsApi->cancelConsignmentById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_id** | **string**| The consignment identifier |
 **body** | [**\Swagger\Client\Model\CancellationRequest**](../Model/CancellationRequest.md)| Consignment data that needs to be stored | [optional]

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConsignmentById**
> \Swagger\Client\Model\Consignment getConsignmentById($carrier_name, $customer_id, $consignment_id, $label_format, $label_size)

Consignment by Id.

Get consignment data from the Freightways system by ConsignmentId

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ConsignmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_id = "consignment_id_example"; // string | The consignment identifier
$label_format = "label_format_example"; // string | Required format of the label - PDF
$label_size = "label_size_example"; // string | Required size of the label - A4, FreThermal

try {
    $result = $apiInstance->getConsignmentById($carrier_name, $customer_id, $consignment_id, $label_format, $label_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsignmentsApi->getConsignmentById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_id** | **string**| The consignment identifier |
 **label_format** | **string**| Required format of the label - PDF | [optional]
 **label_size** | **string**| Required size of the label - A4, FreThermal | [optional]

### Return type

[**\Swagger\Client\Model\Consignment**](../Model/Consignment.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConsignmentsByParameters**
> \Swagger\Client\Model\Consignments getConsignmentsByParameters($carrier_name, $customer_id, $consignment_reference, $consignment_status, $from_consignment_date_time, $to_consignment_date_time, $barcode, $query, $label_format, $label_size, $skip, $limit)

Search consignments based on Consignment / Sender / Receiver details

Search consignments based on Consignment / Sender / Receiver details

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ConsignmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_reference = "consignment_reference_example"; // string | Consignment Reference
$consignment_status = "consignment_status_example"; // string | Consignment Status. Seperate by Comma (,) to search multiple
$from_consignment_date_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When searching within a date range, this is the start time in Utc which you want to search from.
$to_consignment_date_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When searching within a date range, this is the end time in Utc which you want to search to.
$barcode = "barcode_example"; // string | Consignment barcode
$query = "query_example"; // string | Fuzzy search query string
$label_format = "label_format_example"; // string | Required format of the label - PDF
$label_size = "label_size_example"; // string | Required size of the label - A4, FreThermal
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->getConsignmentsByParameters($carrier_name, $customer_id, $consignment_reference, $consignment_status, $from_consignment_date_time, $to_consignment_date_time, $barcode, $query, $label_format, $label_size, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsignmentsApi->getConsignmentsByParameters: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_reference** | **string**| Consignment Reference | [optional]
 **consignment_status** | **string**| Consignment Status. Seperate by Comma (,) to search multiple | [optional]
 **from_consignment_date_time** | **\DateTime**| When searching within a date range, this is the start time in Utc which you want to search from. | [optional]
 **to_consignment_date_time** | **\DateTime**| When searching within a date range, this is the end time in Utc which you want to search to. | [optional]
 **barcode** | **string**| Consignment barcode | [optional]
 **query** | **string**| Fuzzy search query string | [optional]
 **label_format** | **string**| Required format of the label - PDF | [optional]
 **label_size** | **string**| Required size of the label - A4, FreThermal | [optional]
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\Consignments**](../Model/Consignments.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postConsignment**
> \Swagger\Client\Model\ConsignmentRequestResponse postConsignment($carrier_name, $customer_id, $body)

Upload consignment data.

Upload the consignment data into the Freightways system. Returns the consignment id, rate, item barcodes and labels

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ConsignmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$body = new \Swagger\Client\Model\ConsignmentRequest(); // \Swagger\Client\Model\ConsignmentRequest | Consignment data that needs to be stored

try {
    $result = $apiInstance->postConsignment($carrier_name, $customer_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConsignmentsApi->postConsignment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **body** | [**\Swagger\Client\Model\ConsignmentRequest**](../Model/ConsignmentRequest.md)| Consignment data that needs to be stored | [optional]

### Return type

[**\Swagger\Client\Model\ConsignmentRequestResponse**](../Model/ConsignmentRequestResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

