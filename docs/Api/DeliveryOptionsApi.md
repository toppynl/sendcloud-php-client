# Toppy\Sendcloud\DeliveryOptionsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3CheckoutApiGetDeliveryOptions()**](DeliveryOptionsApi.md#scPublicV3CheckoutApiGetDeliveryOptions) | **GET** /checkout/configurations/{configuration_id}/delivery-options | Retrieve a list of delivery options


## `scPublicV3CheckoutApiGetDeliveryOptions()`

```php
scPublicV3CheckoutApiGetDeliveryOptions($configurationId, $weightValue, $totalOrderValue, $fromCountryCode, $toCountryCode, $checkoutIdentifierType, $toPostalCode, $parcelLength, $parcelWidth, $parcelHeight, $checkoutMetadata): \Toppy\Sendcloud\Model\DeliveryOptionsResponse
```

Retrieve a list of delivery options

<!-- theme: success --> >To use this API, you first need to create your own Dynamic Checkout <a href=\"https://support.sendcloud.com/hc/en-us/articles/360057944932-How-to-configure-Dynamic-Checkout\">configuration</a> in the Sendcloud panel. >  Follow these steps to get started:  1. Log in to your Sendcloud account and navigate to the **Dynamic Checkout** tab. 2. Select your API integration from the **Shops** section to customize your delivery options. 3. When you're done, click **Publish** to connect your configuration to the selected API integration.  This API allows your customers to choose their preferred delivery options during checkout. The options returned by this endpoint are based on the <a href=\"https://support.sendcloud.com/hc/en-us/articles/360057944932-How-to-configure-Dynamic-Checkout#4\">delivery methods</a> previously configured in addition to cart or order information, such as parcel weight, total order value, destination country, and more.  You can display the returned delivery options to your customers on your checkout page, where they can select their preferred option for their order.  ### How do delivery options correspond to configured delivery methods? This API returns one delivery option per carrier configured in Dynamic Checkout. If a delivery method is configured with multiple carriers, then multiple delivery options will be returned - one per carrier. In cases when delivery options correspond to the same delivery method, delivery options' ids will refer to the same delivery method id, leaving API users with a flexibility to perform grouping based on a delivery method id, if desired.  ### How can I create a shipment out of the selected delivery option? Use the `checkout_identifier_type=shipping_option_code` parameter when requesting delivery options. This makes the `checkout_identifier` field of the selected delivery option contain the shipping option code required for creating a shipment.  To proceed, call the <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/shipments/operations/create-a-shipment\">Create a shipment</a> endpoint, setting `ship_with.type` to `\"shipping_option_code\"` and `ship_with.properties.shipping_option_code` to the value of the `checkout_identifier` field.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\DeliveryOptionsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$configurationId = 465e2fe8-4589-4ae2-b49c-0c64153e5169; // string | The unique ID of the checkout configuration used to retrieve delivery options
$weightValue = 2500; // int | The total weight of the cart or order, specified in grams by default. This parameter is used to select the most suitable shipping option.
$totalOrderValue = 45.90; // string | The total price of the cart or order, specified in the currency of the checkout configuration. This parameter is used to calculate the shipping rate if rates are configured for the delivery method. It can also be used to determine if free shipping is applicable based on the configured pricing rules.
$fromCountryCode = NULL; // mixed | The sender's country code for the shipment, formatted as an [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code
$toCountryCode = NULL; // mixed | The recipient's country code for the shipment, formatted as an [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code
$checkoutIdentifierType = 'shipping_option_code'; // string | Specifies how to retrieve the shipping label. Currently, only the `shipping_option_code` type is supported.  When this type is used, the `checkout_identifier` field in each delivery option contains the shipping option code, which is required to <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/shipments/operations/create-a-shipment\">create a shipment</a>
$toPostalCode = 5611EM; // string | The recipient's postal code. Use this in combination with <a href=\"https://support.sendcloud.com/hc/en-us/articles/18580048370705-Checkout-rules\">Checkout Rules</a> to show or hide delivery options for specific locations.
$parcelLength = 48; // float | The parcel's length in centimeters (e.g., \"48\" or \"52.3\")
$parcelWidth = 48; // float | The parcel's width in centimeters (e.g., \"48\" or \"52.3\")
$parcelHeight = 48; // float | The parcel's height in centimeters (e.g., \"48\" or \"52.3\")
$checkoutMetadata = demo_sku_12345; // string | An arbitrary text field that can be used with <a href=\"https://support.sendcloud.com/hc/en-us/articles/18580048370705-Checkout-rules\">Checkout Rules</a> to control which delivery options are displayed during checkout. For example, you might use it to pass a product SKU, goods category, or any other custom property to show or hide specific delivery options during checkout

try {
    $result = $apiInstance->scPublicV3CheckoutApiGetDeliveryOptions($configurationId, $weightValue, $totalOrderValue, $fromCountryCode, $toCountryCode, $checkoutIdentifierType, $toPostalCode, $parcelLength, $parcelWidth, $parcelHeight, $checkoutMetadata);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryOptionsApi->scPublicV3CheckoutApiGetDeliveryOptions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configurationId** | **string**| The unique ID of the checkout configuration used to retrieve delivery options |
 **weightValue** | **int**| The total weight of the cart or order, specified in grams by default. This parameter is used to select the most suitable shipping option. |
 **totalOrderValue** | **string**| The total price of the cart or order, specified in the currency of the checkout configuration. This parameter is used to calculate the shipping rate if rates are configured for the delivery method. It can also be used to determine if free shipping is applicable based on the configured pricing rules. |
 **fromCountryCode** | [**mixed**](../Model/.md)| The sender&#39;s country code for the shipment, formatted as an [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code |
 **toCountryCode** | [**mixed**](../Model/.md)| The recipient&#39;s country code for the shipment, formatted as an [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code |
 **checkoutIdentifierType** | **string**| Specifies how to retrieve the shipping label. Currently, only the &#x60;shipping_option_code&#x60; type is supported.  When this type is used, the &#x60;checkout_identifier&#x60; field in each delivery option contains the shipping option code, which is required to &lt;a href&#x3D;\&quot;https://api.sendcloud.dev/docs/sendcloud-public-api/shipments/operations/create-a-shipment\&quot;&gt;create a shipment&lt;/a&gt; | [optional] [default to &#39;shipping_option_code&#39;]
 **toPostalCode** | **string**| The recipient&#39;s postal code. Use this in combination with &lt;a href&#x3D;\&quot;https://support.sendcloud.com/hc/en-us/articles/18580048370705-Checkout-rules\&quot;&gt;Checkout Rules&lt;/a&gt; to show or hide delivery options for specific locations. | [optional]
 **parcelLength** | **float**| The parcel&#39;s length in centimeters (e.g., \&quot;48\&quot; or \&quot;52.3\&quot;) | [optional]
 **parcelWidth** | **float**| The parcel&#39;s width in centimeters (e.g., \&quot;48\&quot; or \&quot;52.3\&quot;) | [optional]
 **parcelHeight** | **float**| The parcel&#39;s height in centimeters (e.g., \&quot;48\&quot; or \&quot;52.3\&quot;) | [optional]
 **checkoutMetadata** | **string**| An arbitrary text field that can be used with &lt;a href&#x3D;\&quot;https://support.sendcloud.com/hc/en-us/articles/18580048370705-Checkout-rules\&quot;&gt;Checkout Rules&lt;/a&gt; to control which delivery options are displayed during checkout. For example, you might use it to pass a product SKU, goods category, or any other custom property to show or hide specific delivery options during checkout | [optional]

### Return type

[**\Toppy\Sendcloud\Model\DeliveryOptionsResponse**](../Model/DeliveryOptionsResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
