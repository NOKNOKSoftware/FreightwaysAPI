# Freightways PHP API
Provisioning Freightways services as REST APIs

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.9
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/NOKNOKSoftware/FreightwaysAPI"
    }
  ],
  "require": {
    "NOKNOKSoftware/FreightwaysAPI": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/FreightwaysAPI/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://customer-integration.ep-customersandbox.freightways.co.nz*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AddressesApi* | [**findAddressAutocomplete**](docs/Api/AddressesApi.md#findaddressautocomplete) | **GET** /v1/addressautocomplete | Returns a list of fuzzy addresses, intended for providing suggestions as you type.
*AddressesApi* | [**findAddressFuzzy**](docs/Api/AddressesApi.md#findaddressfuzzy) | **GET** /v1/addressfuzzy | Fuzzy Search of Address data.
*AddressesApi* | [**findAddressMatch**](docs/Api/AddressesApi.md#findaddressmatch) | **GET** /v1/addressmatch | Returns a list of fuzzy addresses, intended for providing suggestions as you type.
*AddressesApi* | [**getAddressForId**](docs/Api/AddressesApi.md#getaddressforid) | **GET** /v1/addresses/{addressId} | Returns a list of fuzzy addresses, intended for providing suggestions as you type.
*ConsignmentsApi* | [**cancelConsignmentById**](docs/Api/ConsignmentsApi.md#cancelconsignmentbyid) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/cancellationrequests | Request cancellation of a Consignment by Id.
*ConsignmentsApi* | [**getConsignmentById**](docs/Api/ConsignmentsApi.md#getconsignmentbyid) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId} | Consignment by Id.
*ConsignmentsApi* | [**getConsignmentsByParameters**](docs/Api/ConsignmentsApi.md#getconsignmentsbyparameters) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments | Search consignments based on Consignment / Sender / Receiver details
*ConsignmentsApi* | [**postConsignment**](docs/Api/ConsignmentsApi.md#postconsignment) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/consignments | Upload consignment data.
*LabelsApi* | [**getLabelByConsignmentId**](docs/Api/LabelsApi.md#getlabelbyconsignmentid) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/labels | Consignment by Id.
*PickupRequestsApi* | [**createPickupRequest**](docs/Api/PickupRequestsApi.md#createpickuprequest) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/pickup-requests/pickup-location | Lodge a pickup request for the Carrier (carrierName) and customer (customerId) at the provided PickupLocationId
*PickupRequestsApi* | [**createPickupRequestByGeo**](docs/Api/PickupRequestsApi.md#createpickuprequestbygeo) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/pickup-requests/address | PickupRequest the pickup request based on an address
*RatesApi* | [**getStandardRates**](docs/Api/RatesApi.md#getstandardrates) | **POST** /v1/carriers/{carrierName}/customers/{customerId}/rates | Finds rates using the standard Weight or Volume model for a given query
*ServicesApi* | [**getServiceLocations**](docs/Api/ServicesApi.md#getservicelocations) | **GET** /v1/service-locations | Return a list of service locations, optionally filter by location type and/or within a radius of a given point
*ServicesApi* | [**getServices**](docs/Api/ServicesApi.md#getservices) | **GET** /v1/services | Finds available services for a given query
*TrackingEventsApi* | [**getTrackingEvents**](docs/Api/TrackingEventsApi.md#gettrackingevents) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/items/{consignmentItemId}/tracking-events | Finds tracking events by using query string parameters
*TrackingEventsApi* | [**getTrackingEventsAttachment**](docs/Api/TrackingEventsApi.md#gettrackingeventsattachment) | **GET** /v1/carriers/{carrierName}/customers/{customerId}/consignments/{consignmentId}/items/{consignmentItemId}/tracking-events/attachments | Finds attachment for a tracking event

## Documentation For Models

 - [Address](docs/Model/Address.md)
 - [AddressPickupRequest](docs/Model/AddressPickupRequest.md)
 - [BasePlusItemRateRequest](docs/Model/BasePlusItemRateRequest.md)
 - [BasePlusItemRequest](docs/Model/BasePlusItemRequest.md)
 - [BreakdownComponent](docs/Model/BreakdownComponent.md)
 - [CancellationRequest](docs/Model/CancellationRequest.md)
 - [CancellationRequestItem](docs/Model/CancellationRequestItem.md)
 - [CarrierService](docs/Model/CarrierService.md)
 - [CarrierServiceConditions](docs/Model/CarrierServiceConditions.md)
 - [CarrierServiceOptions](docs/Model/CarrierServiceOptions.md)
 - [CarrierServices](docs/Model/CarrierServices.md)
 - [Consignment](docs/Model/Consignment.md)
 - [ConsignmentItem](docs/Model/ConsignmentItem.md)
 - [ConsignmentItemRequestResponse](docs/Model/ConsignmentItemRequestResponse.md)
 - [ConsignmentLabel](docs/Model/ConsignmentLabel.md)
 - [ConsignmentLabelRequest](docs/Model/ConsignmentLabelRequest.md)
 - [ConsignmentRequest](docs/Model/ConsignmentRequest.md)
 - [ConsignmentRequestResponse](docs/Model/ConsignmentRequestResponse.md)
 - [Consignments](docs/Model/Consignments.md)
 - [CustomerReferences](docs/Model/CustomerReferences.md)
 - [Email](docs/Model/Email.md)
 - [Event](docs/Model/Event.md)
 - [Item](docs/Model/Item.md)
 - [Match](docs/Model/Match.md)
 - [Notification](docs/Model/Notification.md)
 - [Notifications](docs/Model/Notifications.md)
 - [PagedResult](docs/Model/PagedResult.md)
 - [PickupLocationPickupRequest](docs/Model/PickupLocationPickupRequest.md)
 - [PickupRequestDetails](docs/Model/PickupRequestDetails.md)
 - [ProblemDetails](docs/Model/ProblemDetails.md)
 - [Rate](docs/Model/Rate.md)
 - [RateOption](docs/Model/RateOption.md)
 - [RatesRequest](docs/Model/RatesRequest.md)
 - [Receiver](docs/Model/Receiver.md)
 - [Run](docs/Model/Run.md)
 - [SatchelItemRateRequest](docs/Model/SatchelItemRateRequest.md)
 - [SatchelItemRequest](docs/Model/SatchelItemRequest.md)
 - [Sender](docs/Model/Sender.md)
 - [ServiceLocation](docs/Model/ServiceLocation.md)
 - [ServiceLocationType](docs/Model/ServiceLocationType.md)
 - [ServiceLocations](docs/Model/ServiceLocations.md)
 - [StandardItemRateRequest](docs/Model/StandardItemRateRequest.md)
 - [StandardItemRequest](docs/Model/StandardItemRequest.md)
 - [TrackingEvent](docs/Model/TrackingEvent.md)
 - [TrackingEventAttachment](docs/Model/TrackingEventAttachment.md)
 - [TrackingEventBase](docs/Model/TrackingEventBase.md)
 - [TrackingEvents](docs/Model/TrackingEvents.md)

## Documentation For Authorization


## oAuth2

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
 - **all**: Grant all rights


## Author



