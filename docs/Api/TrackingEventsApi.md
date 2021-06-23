# Swagger\Client\TrackingEventsApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTrackingEvents**](TrackingEventsApi.md#gettrackingevents) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/items/{consignmentItemId}/tracking-events | Finds tracking events by using query string parameters
[**getTrackingEventsAttachment**](TrackingEventsApi.md#gettrackingeventsattachment) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/items/{consignmentItemId}/tracking-events/attachments | Finds attachment for a tracking event

# **getTrackingEvents**
> \Swagger\Client\Model\TrackingEvents getTrackingEvents($carrier_name, $customer_id, $consignment_id, $consignment_item_id, $events_from, $events_to, $skip, $limit)

Finds tracking events by using query string parameters

Finds tracking events by using query string parameters such as barcode / customer account number / consignment reference / consignment parts / delivery latitude and longitude within a certain radius / by date range

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TrackingEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_id = "consignment_id_example"; // string | Consignment Id
$consignment_item_id = "consignment_item_id_example"; // string | Consignment Item Id
$events_from = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When searching within a date range, this is the start time which you want to search from.
$events_to = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | When searching within a date range, this is the end time which you want to search to.
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->getTrackingEvents($carrier_name, $customer_id, $consignment_id, $consignment_item_id, $events_from, $events_to, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrackingEventsApi->getTrackingEvents: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_id** | **string**| Consignment Id |
 **consignment_item_id** | **string**| Consignment Item Id |
 **events_from** | **\DateTime**| When searching within a date range, this is the start time which you want to search from. | [optional]
 **events_to** | **\DateTime**| When searching within a date range, this is the end time which you want to search to. | [optional]
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\TrackingEvents**](../Model/TrackingEvents.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTrackingEventsAttachment**
> string getTrackingEventsAttachment($carrier_name, $customer_id, $consignment_id, $consignment_item_id, $collection_id, $image_id)

Finds attachment for a tracking event

Finds the attachment for a specified image for a consignment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TrackingEventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | Freightways Carrier
$customer_id = "customer_id_example"; // string | Carrier Customer Id
$consignment_id = "consignment_id_example"; // string | Consignment Id
$consignment_item_id = "consignment_item_id_example"; // string | Consignment Item Id
$collection_id = "collection_id_example"; // string | Collection Id
$image_id = "image_id_example"; // string | Image Id

try {
    $result = $apiInstance->getTrackingEventsAttachment($carrier_name, $customer_id, $consignment_id, $consignment_item_id, $collection_id, $image_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrackingEventsApi->getTrackingEventsAttachment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| Freightways Carrier |
 **customer_id** | **string**| Carrier Customer Id |
 **consignment_id** | **string**| Consignment Id |
 **consignment_item_id** | **string**| Consignment Item Id |
 **collection_id** | **string**| Collection Id |
 **image_id** | **string**| Image Id |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/jpeg, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

