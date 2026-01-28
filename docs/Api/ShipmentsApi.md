# Toppy\Sendcloud\V3\ShipmentsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetAllShipments()**](ShipmentsApi.md#scPublicV3ScpGetAllShipments) | **GET** /shipments | Retrieve shipments
[**scPublicV3ScpGetShipmentById()**](ShipmentsApi.md#scPublicV3ScpGetShipmentById) | **GET** /shipments/{id} | Retrieve a shipment
[**scPublicV3ScpPostAnnounceShipment()**](ShipmentsApi.md#scPublicV3ScpPostAnnounceShipment) | **POST** /shipments/announce | Create and announce a shipment synchronously
[**scPublicV3ScpPostAnnounceShipmentWithRules()**](ShipmentsApi.md#scPublicV3ScpPostAnnounceShipmentWithRules) | **POST** /shipments/announce-with-shipping-rules | Create a shipment with rules and/or defaults and announce it synchronously
[**scPublicV3ScpPostCancelShipment()**](ShipmentsApi.md#scPublicV3ScpPostCancelShipment) | **POST** /shipments/{id}/cancel | Cancel a shipment
[**scPublicV3ScpPostCreateShipment()**](ShipmentsApi.md#scPublicV3ScpPostCreateShipment) | **POST** /shipments | Create and announce a shipment asynchronously
[**scPublicV3ScpPostCreateShipmentWithRules()**](ShipmentsApi.md#scPublicV3ScpPostCreateShipmentWithRules) | **POST** /shipments/create-with-shipping-rules | Create a shipment with rules and/or defaults and announce it asynchronously


## `scPublicV3ScpGetAllShipments()`

```php
scPublicV3ScpGetAllShipments($parcelStatus, $trackingNumber, $externalReferenceId, $orderNumber, $integrationId, $updatedBefore, $updatedAfter, $announcedBefore, $announcedAfter, $ids, $pageSize): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllShipments200Response
```

Retrieve shipments

This endpoint allows you to retrieve a list of all the shipments which you have created or imported into your Sendcloud account under your API credentials. You can filter the results based on several query parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$parcelStatus = new \Toppy\Sendcloud\V3\Model\\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter(); // \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter | Returns shipments that have the requested status. For a list of possible statuses, see the [Retrieve a list of parcel statuses](/api/v3/parcel-statuses/retrieve-a-list-of-parcel-statuses) endpoint.
$trackingNumber = 'trackingNumber_example'; // string | Returns shipments that match a specified tracking number
$externalReferenceId = 'externalReferenceId_example'; // string | Returns shipments that match a specified external reference
$orderNumber = 'orderNumber_example'; // string | Returns a shipment that matches a specific `order_number` property from your shipments
$integrationId = 'integrationId_example'; // string | Returns all shipments that matches a specific `integration_id` property from your shipments
$updatedBefore = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been updated in our system before a given time. Use the ISO 8601 datetime format.
$updatedAfter = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been updated in our system after a given time. Use the ISO 8601 datetime format.
$announcedBefore = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been announced to the carrier before the given time. Use the ISO 8601 datetime format.
$announcedAfter = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been announced to the carrier after the given time. Use the ISO 8601 datetime format.
$ids = 13579,24680,12345; // string | Filter results using a comma-separated list of shipments IDs. The list may not contain more than 100 IDs.
$pageSize = 10; // int | The maximum number of items to be returned in the response.

try {
    $result = $apiInstance->scPublicV3ScpGetAllShipments($parcelStatus, $trackingNumber, $externalReferenceId, $orderNumber, $integrationId, $updatedBefore, $updatedAfter, $announcedBefore, $announcedAfter, $ids, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpGetAllShipments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parcelStatus** | [**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter**](../Model/.md)| Returns shipments that have the requested status. For a list of possible statuses, see the [Retrieve a list of parcel statuses](/api/v3/parcel-statuses/retrieve-a-list-of-parcel-statuses) endpoint. | [optional]
 **trackingNumber** | **string**| Returns shipments that match a specified tracking number | [optional]
 **externalReferenceId** | **string**| Returns shipments that match a specified external reference | [optional]
 **orderNumber** | **string**| Returns a shipment that matches a specific &#x60;order_number&#x60; property from your shipments | [optional]
 **integrationId** | **string**| Returns all shipments that matches a specific &#x60;integration_id&#x60; property from your shipments | [optional]
 **updatedBefore** | **string**| Returns all shipments which have been updated in our system before a given time. Use the ISO 8601 datetime format. | [optional]
 **updatedAfter** | **string**| Returns all shipments which have been updated in our system after a given time. Use the ISO 8601 datetime format. | [optional]
 **announcedBefore** | **string**| Returns all shipments which have been announced to the carrier before the given time. Use the ISO 8601 datetime format. | [optional]
 **announcedAfter** | **string**| Returns all shipments which have been announced to the carrier after the given time. Use the ISO 8601 datetime format. | [optional]
 **ids** | **string**| Filter results using a comma-separated list of shipments IDs. The list may not contain more than 100 IDs. | [optional]
 **pageSize** | **int**| The maximum number of items to be returned in the response. | [optional] [default to 40]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllShipments200Response**](../Model/ScPublicV3ScpGetAllShipments200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetShipmentById()`

```php
scPublicV3ScpGetShipmentById($id): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetShipmentById200Response
```

Retrieve a shipment

This endpoint allows you to retrieve a specific shipment created under your Sendcloud credentials, based on the shipment `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the shipment you want to retrieve

try {
    $result = $apiInstance->scPublicV3ScpGetShipmentById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpGetShipmentById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The id of the shipment you want to retrieve |

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetShipmentById200Response**](../Model/ScPublicV3ScpGetShipmentById200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostAnnounceShipment()`

```php
scPublicV3ScpPostAnnounceShipment($shipmentRequestSyncAnnounce): \Toppy\Sendcloud\V3\Model\AnnouncedShipmentIncludingLabel
```

Create and announce a shipment synchronously

This endpoint **announces a shipment synchronously** under your API credentials.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shipmentRequestSyncAnnounce = {"label_details":{"mime_type":"application/pdf","dpi":72},"to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"label_notes":["I live at the blue door","The doorbell isn't working"],"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\V3\Model\ShipmentRequestSyncAnnounce | 

try {
    $result = $apiInstance->scPublicV3ScpPostAnnounceShipment($shipmentRequestSyncAnnounce);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostAnnounceShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipmentRequestSyncAnnounce** | [**\Toppy\Sendcloud\V3\Model\ShipmentRequestSyncAnnounce**](../Model/ShipmentRequestSyncAnnounce.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\AnnouncedShipmentIncludingLabel**](../Model/AnnouncedShipmentIncludingLabel.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostAnnounceShipmentWithRules()`

```php
scPublicV3ScpPostAnnounceShipmentWithRules($shipmentRequestWithRules): \Toppy\Sendcloud\V3\Model\AnnouncedShipmentIncludingLabel
```

Create a shipment with rules and/or defaults and announce it synchronously

Create and announce a shipment applying shipping rules and/or defaults

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shipmentRequestWithRules = {"apply_shipping_defaults":true,"apply_shipping_rules":true,"delivery_indicator":"DHL home delivery","to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\V3\Model\ShipmentRequestWithRules | 

try {
    $result = $apiInstance->scPublicV3ScpPostAnnounceShipmentWithRules($shipmentRequestWithRules);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostAnnounceShipmentWithRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipmentRequestWithRules** | [**\Toppy\Sendcloud\V3\Model\ShipmentRequestWithRules**](../Model/ShipmentRequestWithRules.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\AnnouncedShipmentIncludingLabel**](../Model/AnnouncedShipmentIncludingLabel.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCancelShipment()`

```php
scPublicV3ScpPostCancelShipment($id): \Toppy\Sendcloud\V3\Model\CancelShipmentStatus
```

Cancel a shipment

Use this endpoint to cancel an announced shipment, if the carrier supports cancellation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the shipment

try {
    $result = $apiInstance->scPublicV3ScpPostCancelShipment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCancelShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| ID of the shipment |

### Return type

[**\Toppy\Sendcloud\V3\Model\CancelShipmentStatus**](../Model/CancelShipmentStatus.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCreateShipment()`

```php
scPublicV3ScpPostCreateShipment($shipmentRequestAsync): \Toppy\Sendcloud\V3\Model\ShipmentCreatedResponse
```

Create and announce a shipment asynchronously

This endpoint **announces a shipment asynchronously** under your API credentials.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shipmentRequestAsync = {"to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\V3\Model\ShipmentRequestAsync | 

try {
    $result = $apiInstance->scPublicV3ScpPostCreateShipment($shipmentRequestAsync);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCreateShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipmentRequestAsync** | [**\Toppy\Sendcloud\V3\Model\ShipmentRequestAsync**](../Model/ShipmentRequestAsync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ShipmentCreatedResponse**](../Model/ShipmentCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCreateShipmentWithRules()`

```php
scPublicV3ScpPostCreateShipmentWithRules($shipmentRequestWithRules): \Toppy\Sendcloud\V3\Model\ShipmentCreatedResponse
```

Create a shipment with rules and/or defaults and announce it asynchronously

Create and announce a shipment applying shipping rules and/or defaults asynchronously.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shipmentRequestWithRules = {"apply_shipping_defaults":true,"apply_shipping_rules":true,"delivery_indicator":"DHL home delivery","to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":"12.65","currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\V3\Model\ShipmentRequestWithRules | 

try {
    $result = $apiInstance->scPublicV3ScpPostCreateShipmentWithRules($shipmentRequestWithRules);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCreateShipmentWithRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipmentRequestWithRules** | [**\Toppy\Sendcloud\V3\Model\ShipmentRequestWithRules**](../Model/ShipmentRequestWithRules.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ShipmentCreatedResponse**](../Model/ShipmentCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
