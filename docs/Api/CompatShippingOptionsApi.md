# Toppy\Sendcloud\CompatShippingOptionsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpPostCompatShippingOptions()**](CompatShippingOptionsApi.md#scPublicV3ScpPostCompatShippingOptions) | **POST** /compat/shipping-options | Retrieve a list of shipping options


## `scPublicV3ScpPostCompatShippingOptions()`

```php
scPublicV3ScpPostCompatShippingOptions($scPublicV3ScpPostCompatShippingOptionsRequest): \Toppy\Sendcloud\Model\CompatShippingOptionsResponse
```

Retrieve a list of shipping options

Retrieve a list of shipping options based on the provided shipping method ids.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CompatShippingOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3ScpPostCompatShippingOptionsRequest = new \Toppy\Sendcloud\Model\ScPublicV3ScpPostCompatShippingOptionsRequest(); // \Toppy\Sendcloud\Model\ScPublicV3ScpPostCompatShippingOptionsRequest

try {
    $result = $apiInstance->scPublicV3ScpPostCompatShippingOptions($scPublicV3ScpPostCompatShippingOptionsRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompatShippingOptionsApi->scPublicV3ScpPostCompatShippingOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3ScpPostCompatShippingOptionsRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostCompatShippingOptionsRequest**](../Model/ScPublicV3ScpPostCompatShippingOptionsRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\CompatShippingOptionsResponse**](../Model/CompatShippingOptionsResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
