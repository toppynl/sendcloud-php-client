# Toppy\Sendcloud\ShippingOptionsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpPostShippingOptions()**](ShippingOptionsApi.md#scPublicV3ScpPostShippingOptions) | **POST** /shipping-options | Return a list of available shipping options [BETA]
[**scPublicV3ScpPostShippingOptionsSimple()**](ShippingOptionsApi.md#scPublicV3ScpPostShippingOptionsSimple) | **POST** /fetch-shipping-options | Create a list of shipping options


## `scPublicV3ScpPostShippingOptions()`

```php
scPublicV3ScpPostShippingOptions($shippingOptionFilter): \Toppy\Sendcloud\Model\ScPublicV3ScpPostShippingOptions200Response
```

Return a list of available shipping options [BETA]

This API endpoint allows you to retrieve available shipping options along with their corresponding prices for entire shipments, supporting multicollo as well.  Unlike the fetch-shipping-options endpoint, this endpoint: - Accepts multiple parcels with individual dimensions and weights - Returns total pricing for the entire shipment  You must have either [**enabled a carrier**](https://sendcloud.dev/docs/getting-started/) in your Sendcloud account, or connected your own direct [**carrier contract**](https://sendcloud.dev/docs/getting-started/carrier-contracts/), in order to be able to retrieve shipping options related to that carrier via this endpoint.  When shipping to a remote area, it's possible that a remote surcharge will be invoiced. Make sure to provide the `from_country_code`, `to_country_code` and `to_postal_code` to see remote surcharges in the price breakdown. Similarly, to access **zonal prices**, provide `from_country_code`, `to_country_code`, `from_postal_code`, and `to_postal_code`.  When neither `to_country_code` nor `from_country_code` are provided, the shipping options will be returned without quotes irrespective of the value you pass into `calculate_quotes`.  ### Development status This endpoint is currently in <a href=\"https://support.sendcloud.com/hc/en-us/articles/4417167140756-What-is-beta-\">**beta**</a>, meaning that it is still under development. During this phase, we continually monitor and test the API to improve its performance, review the requested and the returned data, and uncover any potential bugs that could have a future impact on our users.   <!-- theme: warning --> >**Please note that there is a possibility of experiencing breaking changes while it is still in beta**.  Last updated at: 17-09-2025.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShippingOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$shippingOptionFilter = {"from_country_code":"NL","to_country_code":"NL","from_postal_code":"1012AB","to_postal_code":"2000AB","parcels":[{"dimensions":{"length":"30","width":"20","height":"15","unit":"cm"},"weight":{"value":"2","unit":"kg"},"additional_insured_price":{"value":"50.00","currency":"EUR"}},{"dimensions":{"length":"25","width":"18","height":"12","unit":"cm"},"weight":{"value":"1.5","unit":"kg"},"total_insured_price":{"value":"100.00","currency":"EUR"}}],"carrier_code":"postnl","functionalities":{"signature":true},"calculate_quotes":true}; // \Toppy\Sendcloud\Model\ShippingOptionFilter | Shipment details for quote calculation

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
 **shippingOptionFilter** | [**\Toppy\Sendcloud\Model\ShippingOptionFilter**](../Model/ShippingOptionFilter.md)| Shipment details for quote calculation | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostShippingOptions200Response**](../Model/ScPublicV3ScpPostShippingOptions200Response.md)

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
scPublicV3ScpPostShippingOptionsSimple($singleParcelShippingOptionFilter): \Toppy\Sendcloud\Model\ScPublicV3ScpPostShippingOptionsSimple200Response
```

Create a list of shipping options

This API endpoint allows you to retrieve available shipping options along with their corresponding prices, referred to as shipping quotes.  A shipping option is a shipping product that the carrier offers in combination with a unique set of shipping functionalities.  The quotes serve to indicate the cost of this shipping option.   You must have either [**enabled a carrier**](https://sendcloud.dev/docs/getting-started/) in your Sendcloud account, or connected your own direct [**carrier contract**](https://sendcloud.dev/docs/getting-started/carrier-contracts/), in order to be able to retrieve shipping options related to that carrier via this endpoint.   When shipping to a remote area, it's possible that a remote surcharge will be invoiced. Make sure to provide the `from_country_code`, `to_country_code` and `to_postal_code` to see remote surcharges in the price breakdown. Similarly, to access **zonal prices**, provide `from_country_code`, `to_country_code`, `from_postal_code`, and `to_postal_code`. This information ensures accurate and customized pricing based on the specific location, enabling you to understand any additional charges associated with remote areas and access pricing based on their designated zones.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShippingOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$singleParcelShippingOptionFilter = {"from_country_code":"NL","to_country_code":"NL","weight":{"value":"2","unit":"kg"},"carrier_code":"postnl","functionalities":{"signature":true}}; // \Toppy\Sendcloud\Model\SingleParcelShippingOptionFilter | 

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
 **singleParcelShippingOptionFilter** | [**\Toppy\Sendcloud\Model\SingleParcelShippingOptionFilter**](../Model/SingleParcelShippingOptionFilter.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostShippingOptionsSimple200Response**](../Model/ScPublicV3ScpPostShippingOptionsSimple200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
