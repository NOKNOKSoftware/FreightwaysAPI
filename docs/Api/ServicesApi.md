# Swagger\Client\ServicesApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getServiceLocations**](ServicesApi.md#getservicelocations) | **GET** /v1/service-locations | Return a list of service locations, optionally filter by location type and/or within a radius of a given point
[**getServices**](ServicesApi.md#getservices) | **GET** /v1/services | Finds available services for a given query

# **getServiceLocations**
> \Swagger\Client\Model\ServiceLocations getServiceLocations($carrier_name, $lat, $lon, $service_location_type, $radius, $skip, $limit)

Return a list of service locations, optionally filter by location type and/or within a radius of a given point

Return a list of service locations, optionally filter by location type and/or within a radius of a given point

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ServicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$carrier_name = "carrier_name_example"; // string | The carrier ID for which to provide a list of available services.
$lat = 1.2; // double | The latitude for which to provide a list of available services. Requires lon & radius.
$lon = 1.2; // double | The longitude for which to provide a list of available services. Requires lat & radius.
$service_location_type = "service_location_type_example"; // string | The type of service location (e.g. Agent, Depot).
$radius = 56; // int | The distance in metres from the geo point the service point must be within. Requires lat & lon.
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->getServiceLocations($carrier_name, $lat, $lon, $service_location_type, $radius, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServicesApi->getServiceLocations: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrier_name** | **string**| The carrier ID for which to provide a list of available services. | [optional]
 **lat** | **double**| The latitude for which to provide a list of available services. Requires lon &amp; radius. | [optional]
 **lon** | **double**| The longitude for which to provide a list of available services. Requires lat &amp; radius. | [optional]
 **service_location_type** | **string**| The type of service location (e.g. Agent, Depot). | [optional]
 **radius** | **int**| The distance in metres from the geo point the service point must be within. Requires lat &amp; lon. | [optional]
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\ServiceLocations**](../Model/ServiceLocations.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getServices**
> \Swagger\Client\Model\CarrierServices getServices($lat, $lon, $carrier_name)

Finds available services for a given query

Finds available services for a given query

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ServicesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$lat = 1.2; // double | The latitude for which to provide a list of available services. Requires lon.
$lon = 1.2; // double | The longitude for which to provide a list of available services. Requires lat.
$carrier_name = "carrier_name_example"; // string | The carrier ID for which to provide a list of available services.  If not provided all carriers will be returned.

try {
    $result = $apiInstance->getServices($lat, $lon, $carrier_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServicesApi->getServices: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lat** | **double**| The latitude for which to provide a list of available services. Requires lon. |
 **lon** | **double**| The longitude for which to provide a list of available services. Requires lat. |
 **carrier_name** | **string**| The carrier ID for which to provide a list of available services.  If not provided all carriers will be returned. | [optional]

### Return type

[**\Swagger\Client\Model\CarrierServices**](../Model/CarrierServices.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

