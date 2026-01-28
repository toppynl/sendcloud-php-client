# Toppy\Sendcloud\V3\ShipAnOrderApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3OrdersLabelsPostCreateLabelsAsync()**](ShipAnOrderApi.md#scPublicV3OrdersLabelsPostCreateLabelsAsync) | **POST** /orders/create-labels-async | Request a label for one or more orders asynchronously
[**scPublicV3OrdersLabelsPostCreateLabelsSync()**](ShipAnOrderApi.md#scPublicV3OrdersLabelsPostCreateLabelsSync) | **POST** /orders/create-label-sync | Request a label for a single order synchronously


## `scPublicV3OrdersLabelsPostCreateLabelsAsync()`

```php
scPublicV3OrdersLabelsPostCreateLabelsAsync($sendcloudPartnerId, $createLabelsAsync): \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response
```

Request a label for one or more orders asynchronously

Request a label for a single or multiple orders. This endpoint will fail gracefully if some orders cannot be processed, returning any successfully created labels along with error details for the orders that failed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipAnOrderApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$createLabelsAsync = {"integration_id":70,"orders":[{"order_number":"ORDER-25763","apply_shipping_rules":false}]}; // \Toppy\Sendcloud\V3\Model\CreateLabelsAsync

try {
    $result = $apiInstance->scPublicV3OrdersLabelsPostCreateLabelsAsync($sendcloudPartnerId, $createLabelsAsync);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipAnOrderApi->scPublicV3OrdersLabelsPostCreateLabelsAsync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **createLabelsAsync** | [**\Toppy\Sendcloud\V3\Model\CreateLabelsAsync**](../Model/CreateLabelsAsync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response**](../Model/ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3OrdersLabelsPostCreateLabelsSync()`

```php
scPublicV3OrdersLabelsPostCreateLabelsSync($sendcloudPartnerId, $createLabelsSync): \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersLabelsPostCreateLabelsSync201Response
```

Request a label for a single order synchronously

Request a label for a single order and wait for the results. The label and any other documents will be provided in the response to this request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShipAnOrderApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$createLabelsSync = {"integration_id":70,"label_details":{"mime_type":"application/pdf","dpi":72},"order":{"order_number":"ORDER-25763","apply_shipping_rules":false}}; // \Toppy\Sendcloud\V3\Model\CreateLabelsSync

try {
    $result = $apiInstance->scPublicV3OrdersLabelsPostCreateLabelsSync($sendcloudPartnerId, $createLabelsSync);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipAnOrderApi->scPublicV3OrdersLabelsPostCreateLabelsSync: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **createLabelsSync** | [**\Toppy\Sendcloud\V3\Model\CreateLabelsSync**](../Model/CreateLabelsSync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersLabelsPostCreateLabelsSync201Response**](../Model/ScPublicV3OrdersLabelsPostCreateLabelsSync201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
