# Toppy\Sendcloud\ParcelTrackingApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber()**](ParcelTrackingApi.md#scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber) | **GET** /parcels/tracking/{tracking_number} | Retrieve tracking information for a parcel
[**scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking()**](ParcelTrackingApi.md#scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking) | **POST** /parcels/tracking | Create a tracking-only parcel


## `scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber()`

```php
scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber($trackingNumber): \Toppy\Sendcloud\Model\ParcelTrackingResponse
```

Retrieve tracking information for a parcel

Get information about a parcel, including its current status and recent tracking events, using its tracking number

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ParcelTrackingApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$trackingNumber = 'trackingNumber_example'; // string | Parcel tracking number

try {
    $result = $apiInstance->scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber($trackingNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ParcelTrackingApi->scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **trackingNumber** | **string**| Parcel tracking number |

### Return type

[**\Toppy\Sendcloud\Model\ParcelTrackingResponse**](../Model/ParcelTrackingResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking()`

```php
scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking($parcelTrackingCreateRequest): \Toppy\Sendcloud\Model\ParcelTrackingCreateResponse
```

Create a tracking-only parcel

Register a parcel in the Sendcloud system for Tracking-Only, based on the provided details. It requires a valid tracking number and parcel information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ParcelTrackingApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$parcelTrackingCreateRequest = new \Toppy\Sendcloud\Model\ParcelTrackingCreateRequest(); // \Toppy\Sendcloud\Model\ParcelTrackingCreateRequest

try {
    $result = $apiInstance->scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking($parcelTrackingCreateRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ParcelTrackingApi->scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parcelTrackingCreateRequest** | [**\Toppy\Sendcloud\Model\ParcelTrackingCreateRequest**](../Model/ParcelTrackingCreateRequest.md)|  |

### Return type

[**\Toppy\Sendcloud\Model\ParcelTrackingCreateResponse**](../Model/ParcelTrackingCreateResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
