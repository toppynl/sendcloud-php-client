# Toppy\Sendcloud\ShipAnOrderApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3OrdersLabelsPostCreateLabelsAsync()**](ShipAnOrderApi.md#scPublicV3OrdersLabelsPostCreateLabelsAsync) | **POST** /orders/create-labels-async | Request a label for given orders asynchronously.
[**scPublicV3OrdersLabelsPostCreateLabelsSync()**](ShipAnOrderApi.md#scPublicV3OrdersLabelsPostCreateLabelsSync) | **POST** /orders/create-label-sync | Request a label for given order synchronously.


## `scPublicV3OrdersLabelsPostCreateLabelsAsync()`

```php
scPublicV3OrdersLabelsPostCreateLabelsAsync($sendcloudPartnerId, $createLabelsAsync): \Toppy\Sendcloud\Model\ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response
```

Request a label for given orders asynchronously.

Request a label for a single or multiple orders. To retrieve your documents or view the announcement errors, call the `/shipments/{id}` endpoint to find out their location, for more detail visit <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipments/operations/get-a-shipment\">**ShipmentAPI**</a>  To apply shipping rules on the provided orders a `apply_shipping_rules` needs to be set to true. Each label will be tried to be generated. If a request for a label runs into an error, other labels will still be attempted to be generated. Because of this, both generated labels and errors can be returned in a single request. Use the errors source -> pointer to see which labels encountered a problem.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipAnOrderApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | Send an additional request header for the system to recognize you if you are an official <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\">**Sendcloud Tech Partner**</a>. Sendcloud Partner UUID is provided to Sendcloud partners.
$createLabelsAsync = {"integration_id":70,"orders":[{"order_number":"ORDER-25763","apply_shipping_rules":false}]}; // \Toppy\Sendcloud\Model\CreateLabelsAsync

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
 **sendcloudPartnerId** | **string**| Send an additional request header for the system to recognize you if you are an official &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;**Sendcloud Tech Partner**&lt;/a&gt;. Sendcloud Partner UUID is provided to Sendcloud partners. | [optional]
 **createLabelsAsync** | [**\Toppy\Sendcloud\Model\CreateLabelsAsync**](../Model/CreateLabelsAsync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response**](../Model/ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response.md)

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
scPublicV3OrdersLabelsPostCreateLabelsSync($sendcloudPartnerId, $createLabelsSync): \Toppy\Sendcloud\Model\ScPublicV3OrdersLabelsPostCreateLabelsSync201Response
```

Request a label for given order synchronously.

Request a label for an order, the documents will be provided in response to this request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipAnOrderApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | Send an additional request header for the system to recognize you if you are an official <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\">**Sendcloud Tech Partner**</a>. Sendcloud Partner UUID is provided to Sendcloud partners.
$createLabelsSync = {"integration_id":70,"label_details":{"mime_type":"application/pdf","dpi":72},"order":{"order_number":"ORDER-25763","apply_shipping_rules":false}}; // \Toppy\Sendcloud\Model\CreateLabelsSync

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
 **sendcloudPartnerId** | **string**| Send an additional request header for the system to recognize you if you are an official &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;**Sendcloud Tech Partner**&lt;/a&gt;. Sendcloud Partner UUID is provided to Sendcloud partners. | [optional]
 **createLabelsSync** | [**\Toppy\Sendcloud\Model\CreateLabelsSync**](../Model/CreateLabelsSync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersLabelsPostCreateLabelsSync201Response**](../Model/ScPublicV3OrdersLabelsPostCreateLabelsSync201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
