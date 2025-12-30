# Toppy\Sendcloud\CreateTicketApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3DsfPostTicketsAddressChange()**](CreateTicketApi.md#scPublicV3DsfPostTicketsAddressChange) | **POST** /dsf/tickets/address-change | Create ticket for an address change
[**scPublicV3DsfPostTicketsDamage()**](CreateTicketApi.md#scPublicV3DsfPostTicketsDamage) | **POST** /dsf/tickets/damage | Create ticket for a damaged parcel
[**scPublicV3DsfPostTicketsDelay()**](CreateTicketApi.md#scPublicV3DsfPostTicketsDelay) | **POST** /dsf/tickets/delay | Create ticket for a delayed parcel
[**scPublicV3DsfPostTicketsDeliveredButNotReceived()**](CreateTicketApi.md#scPublicV3DsfPostTicketsDeliveredButNotReceived) | **POST** /dsf/tickets/delivered-but-not-received | Create ticket for a delivered but not received parcel
[**scPublicV3DsfPostTicketsLost()**](CreateTicketApi.md#scPublicV3DsfPostTicketsLost) | **POST** /dsf/tickets/lost | Create ticket for a lost parcel
[**scPublicV3DsfPostTicketsUnjustReturn()**](CreateTicketApi.md#scPublicV3DsfPostTicketsUnjustReturn) | **POST** /dsf/tickets/unjust-return | Create ticket for an unjustly returned parcel


## `scPublicV3DsfPostTicketsAddressChange()`

```php
scPublicV3DsfPostTicketsAddressChange($scPublicV3DsfPostTicketsAddressChangeRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for an address change

This method allows you to create a ticket for an address change. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsAddressChangeRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsAddressChangeRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsAddressChangeRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsAddressChange($scPublicV3DsfPostTicketsAddressChangeRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsAddressChange: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsAddressChangeRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsAddressChangeRequest**](../Model/ScPublicV3DsfPostTicketsAddressChangeRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostTicketsDamage()`

```php
scPublicV3DsfPostTicketsDamage($scPublicV3DsfPostTicketsDamageRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for a damaged parcel

This method allows you to create a ticket for a damaged parcel. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsDamageRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDamageRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDamageRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsDamage($scPublicV3DsfPostTicketsDamageRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsDamage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsDamageRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDamageRequest**](../Model/ScPublicV3DsfPostTicketsDamageRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostTicketsDelay()`

```php
scPublicV3DsfPostTicketsDelay($scPublicV3DsfPostTicketsDelayRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for a delayed parcel

This method allows you to create a ticket for a delayed parcel. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsDelayRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDelayRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDelayRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsDelay($scPublicV3DsfPostTicketsDelayRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsDelay: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsDelayRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDelayRequest**](../Model/ScPublicV3DsfPostTicketsDelayRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostTicketsDeliveredButNotReceived()`

```php
scPublicV3DsfPostTicketsDeliveredButNotReceived($scPublicV3DsfPostTicketsDeliveredButNotReceivedRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for a delivered but not received parcel

This method allows you to create a ticket for a delivered but not received parcel. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsDeliveredButNotReceivedRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsDeliveredButNotReceived($scPublicV3DsfPostTicketsDeliveredButNotReceivedRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsDeliveredButNotReceived: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsDeliveredButNotReceivedRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest**](../Model/ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostTicketsLost()`

```php
scPublicV3DsfPostTicketsLost($scPublicV3DsfPostTicketsLostRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for a lost parcel

This method allows you to create a ticket for a lost parcel. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsLostRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsLostRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsLostRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsLost($scPublicV3DsfPostTicketsLostRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsLost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsLostRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsLostRequest**](../Model/ScPublicV3DsfPostTicketsLostRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostTicketsUnjustReturn()`

```php
scPublicV3DsfPostTicketsUnjustReturn($scPublicV3DsfPostTicketsUnjustReturnRequest): \Toppy\Sendcloud\Model\CreateTicketResponseSchema
```

Create ticket for an unjustly returned parcel

This method allows you to create a ticket for an unjustly returned parcel. It works with both your own contract and parcels created using Sendcloud rates.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CreateTicketApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostTicketsUnjustReturnRequest = new \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsUnjustReturnRequest(); // \Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsUnjustReturnRequest | Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below.

try {
    $result = $apiInstance->scPublicV3DsfPostTicketsUnjustReturn($scPublicV3DsfPostTicketsUnjustReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateTicketApi->scPublicV3DsfPostTicketsUnjustReturn: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostTicketsUnjustReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostTicketsUnjustReturnRequest**](../Model/ScPublicV3DsfPostTicketsUnjustReturnRequest.md)| Data that is needed for creation of a ticket for own contract parcel and parcels created using Sendcloud rates is different. Please refer to relevant examples below. |

### Return type

[**\Toppy\Sendcloud\Model\CreateTicketResponseSchema**](../Model/CreateTicketResponseSchema.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
