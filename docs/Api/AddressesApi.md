# Swagger\Client\AddressesApi

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Method | HTTP request | Description
------------- | ------------- | -------------
[**findAddressAutocomplete**](AddressesApi.md#findaddressautocomplete) | **GET** /v1/addressautocomplete | Returns a list of fuzzy addresses, intended for providing suggestions as you type.
[**findAddressFuzzy**](AddressesApi.md#findaddressfuzzy) | **GET** /v1/addressfuzzy | Fuzzy Search of Address data.
[**findAddressMatch**](AddressesApi.md#findaddressmatch) | **GET** /v1/addressmatch | Returns a list of fuzzy addresses, intended for providing suggestions as you type.
[**getAddressForId**](AddressesApi.md#getaddressforid) | **GET** /v1/addresses/{addressId} | Returns a list of fuzzy addresses, intended for providing suggestions as you type.

# **findAddressAutocomplete**
> \Swagger\Client\Model\Match[] findAddressAutocomplete($query, $skip, $limit)

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$query = "query_example"; // string | Query text for providing suggestions on. For the default prefix match type, this can be thought of an 'addresses starting with this text' search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down.
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->findAddressAutocomplete($query, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->findAddressAutocomplete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string**| Query text for providing suggestions on. For the default prefix match type, this can be thought of an &#x27;addresses starting with this text&#x27; search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down. |
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\Match[]**](../Model/Match.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAddressFuzzy**
> \Swagger\Client\Model\Match[] findAddressFuzzy($query, $skip, $limit)

Fuzzy Search of Address data.

Returns a list of matching addresses and id's, addresses are matched using fuzzy

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$query = "query_example"; // string | Query text for providing suggestions on. For the default prefix match type, this can be thought of an 'addresses starting with this text' search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down.
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->findAddressFuzzy($query, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->findAddressFuzzy: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string**| Query text for providing suggestions on. For the default prefix match type, this can be thought of an &#x27;addresses starting with this text&#x27; search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down. |
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\Match[]**](../Model/Match.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAddressMatch**
> \Swagger\Client\Model\Match[] findAddressMatch($query, $skip, $limit)

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$query = "query_example"; // string | Query text for providing suggestions on. For the default prefix match type, this can be thought of an 'addresses starting with this text' search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down.
$skip = 0; // int | number of records to skip for pagination
$limit = 10; // int | maximum number of records to return

try {
    $result = $apiInstance->findAddressMatch($query, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->findAddressMatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **string**| Query text for providing suggestions on. For the default prefix match type, this can be thought of an &#x27;addresses starting with this text&#x27; search e.g. (10A Vict) matches streets starting with 10A Victoria and 10A Victor. The more text provided (or typed by a user for example), the more the results will be narrowed down. |
 **skip** | **int**| number of records to skip for pagination | [optional] [default to 0]
 **limit** | **int**| maximum number of records to return | [optional] [default to 10]

### Return type

[**\Swagger\Client\Model\Match[]**](../Model/Match.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAddressForId**
> \Swagger\Client\Model\Address getAddressForId($address_id)

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

Returns a list of fuzzy addresses, intended for providing suggestions as you type.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$address_id = "address_id_example"; // string | Returns an address for an id

try {
    $result = $apiInstance->getAddressForId($address_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->getAddressForId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address_id** | **string**| Returns an address for an id |

### Return type

[**\Swagger\Client\Model\Address**](../Model/Address.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

