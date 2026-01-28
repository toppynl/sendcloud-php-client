# Toppy\Sendcloud\V3\ShippingOptionsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpPostShippingOptions()**](ShippingOptionsApi.md#scPublicV3ScpPostShippingOptions) | **POST** /shipping-options | Return a list of available shipping options
[**scPublicV3ScpPostShippingOptionsSimple()**](ShippingOptionsApi.md#scPublicV3ScpPostShippingOptionsSimple) | **POST** /fetch-shipping-options | Create a list of shipping options


## `scPublicV3ScpPostShippingOptions()`

```php
scPublicV3ScpPostShippingOptions($shippingOptionFilter): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostShippingOptions200Response
```

Return a list of available shipping options

Retrieve available shipping options along with their corresponding prices for entire shipments, supporting multicollo as well.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShippingOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shippingOptionFilter = {"from_country_code":"NL","to_country_code":"NL","from_postal_code":"1012AB","to_postal_code":"2000AB","parcels":[{"dimensions":{"length":"30","width":"20","height":"15","unit":"cm"},"weight":{"value":"2","unit":"kg"},"additional_insured_price":{"value":"50.00","currency":"EUR"}},{"dimensions":{"length":"25","width":"18","height":"12","unit":"cm"},"weight":{"value":"1.5","unit":"kg"},"total_insured_price":{"value":"100.00","currency":"EUR"}}],"carrier_code":"postnl","functionalities":{"signature":true},"calculate_quotes":true}; // \Toppy\Sendcloud\V3\Model\ShippingOptionFilter | Shipment details for quote calculation

try {
    $result = $apiInstance->scPublicV3ScpPostShippingOptions($shippingOptionFilter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingOptionsApi->scPublicV3ScpPostShippingOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shippingOptionFilter** | [**\Toppy\Sendcloud\V3\Model\ShippingOptionFilter**](../Model/ShippingOptionFilter.md)| Shipment details for quote calculation | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostShippingOptions200Response**](../Model/ScPublicV3ScpPostShippingOptions200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostShippingOptionsSimple()`

```php
scPublicV3ScpPostShippingOptionsSimple($singleParcelShippingOptionFilter): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostShippingOptionsSimple200Response
```

Create a list of shipping options

Allows you to retrieve available shipping options along with their corresponding prices, referred to as shipping quotes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ShippingOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$singleParcelShippingOptionFilter = {"from_country_code":"NL","to_country_code":"NL","weight":{"value":"2","unit":"kg"},"carrier_code":"postnl","functionalities":{"signature":true}}; // \Toppy\Sendcloud\V3\Model\SingleParcelShippingOptionFilter | 

try {
    $result = $apiInstance->scPublicV3ScpPostShippingOptionsSimple($singleParcelShippingOptionFilter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingOptionsApi->scPublicV3ScpPostShippingOptionsSimple: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **singleParcelShippingOptionFilter** | [**\Toppy\Sendcloud\V3\Model\SingleParcelShippingOptionFilter**](../Model/SingleParcelShippingOptionFilter.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostShippingOptionsSimple200Response**](../Model/ScPublicV3ScpPostShippingOptionsSimple200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
