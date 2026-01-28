# Toppy\Sendcloud\V3\DeliveryOptionsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3CheckoutApiGetDeliveryOptions()**](DeliveryOptionsApi.md#scPublicV3CheckoutApiGetDeliveryOptions) | **GET** /checkout/configurations/{configuration_id}/delivery-options | Retrieve a list of delivery options


## `scPublicV3CheckoutApiGetDeliveryOptions()`

```php
scPublicV3CheckoutApiGetDeliveryOptions($configurationId): \Toppy\Sendcloud\V3\Model\DeliveryOptionsResponse
```

Retrieve a list of delivery options

The options returned by this endpoint are based on the [delivery methods](https://support.sendcloud.com/hc/en-us/articles/360057944932-How-to-configure-Dynamic-Checkout#4) previously configured in addition to cart or order information, such as parcel weight, total order value, destination country, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\DeliveryOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$configurationId = 'configurationId_example'; // string | The checkout configuration ID

try {
    $result = $apiInstance->scPublicV3CheckoutApiGetDeliveryOptions($configurationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryOptionsApi->scPublicV3CheckoutApiGetDeliveryOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configurationId** | **string**| The checkout configuration ID |

### Return type

[**\Toppy\Sendcloud\V3\Model\DeliveryOptionsResponse**](../Model/DeliveryOptionsResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
