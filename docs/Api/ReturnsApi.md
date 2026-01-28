# Toppy\Sendcloud\V3\ReturnsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetReturnsGetDetails()**](ReturnsApi.md#scPublicV3ScpGetReturnsGetDetails) | **GET** /returns/{id} | Retrieve a return
[**scPublicV3ScpGetReturnsGetReturns()**](ReturnsApi.md#scPublicV3ScpGetReturnsGetReturns) | **GET** /returns | Retrieve a list of returns
[**scPublicV3ScpPatchReturnsCancel()**](ReturnsApi.md#scPublicV3ScpPatchReturnsCancel) | **PATCH** /returns/{id}/cancel | Request cancellation of a return
[**scPublicV3ScpPostReturnsCreateNewReturn()**](ReturnsApi.md#scPublicV3ScpPostReturnsCreateNewReturn) | **POST** /returns | Create a return
[**scPublicV3ScpPostReturnsCreateNewReturnSynchronously()**](ReturnsApi.md#scPublicV3ScpPostReturnsCreateNewReturnSynchronously) | **POST** /returns/announce-synchronously | Create a return synchronously
[**scPublicV3ScpPostReturnsValidate()**](ReturnsApi.md#scPublicV3ScpPostReturnsValidate) | **POST** /returns/validate | Validate a return


## `scPublicV3ScpGetReturnsGetDetails()`

```php
scPublicV3ScpGetReturnsGetDetails($id): \Toppy\Sendcloud\V3\Model\ModelReturn
```

Retrieve a return

Retrieve information about a specific return parcel based on the return `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1751075; // int | The internal Sendcloud id of this return

try {
    $result = $apiInstance->scPublicV3ScpGetReturnsGetDetails($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpGetReturnsGetDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The internal Sendcloud id of this return |

### Return type

[**\Toppy\Sendcloud\V3\Model\ModelReturn**](../Model/ModelReturn.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetReturnsGetReturns()`

```php
scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $parentParcelStatus, $pageSize): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetReturnsGetReturns200Response
```

Retrieve a list of returns

Retrieve a list of returns which have been created under your API credentials.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$fromDate = 2022-04-06 00:00:00; // string | Excludes all returns before this datetime
$toDate = 2022-04-07 00:00:00; // string | Excludes all returns after this datetime
$parentParcelStatus = announced; // string | Search for returns with this parent status
$pageSize = 10; // float | Refers to the number of items per page

try {
    $result = $apiInstance->scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $parentParcelStatus, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpGetReturnsGetReturns: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fromDate** | **string**| Excludes all returns before this datetime |
 **toDate** | **string**| Excludes all returns after this datetime |
 **parentParcelStatus** | **string**| Search for returns with this parent status | [optional]
 **pageSize** | **float**| Refers to the number of items per page | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetReturnsGetReturns200Response**](../Model/ScPublicV3ScpGetReturnsGetReturns200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPatchReturnsCancel()`

```php
scPublicV3ScpPatchReturnsCancel($id): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPatchReturnsCancel202Response
```

Request cancellation of a return

You can request cancellation for a return by providing the return `id` to this endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1751075; // int | The internal Sendcloud id of this return

try {
    $result = $apiInstance->scPublicV3ScpPatchReturnsCancel($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPatchReturnsCancel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The internal Sendcloud id of this return |

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPatchReturnsCancel202Response**](../Model/ScPublicV3ScpPatchReturnsCancel202Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsCreateNewReturn()`

```php
scPublicV3ScpPostReturnsCreateNewReturn(): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return

Create a standalone return

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturn();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturn: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsCreateNewReturnSynchronously()`

```php
scPublicV3ScpPostReturnsCreateNewReturnSynchronously(): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return synchronously

Create a return synchronously, i.e. wait for a response from the carrier before continuing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturnSynchronously();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturnSynchronously: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsValidate()`

```php
scPublicV3ScpPostReturnsValidate(): \Toppy\Sendcloud\V3\Model\ReturnValidation
```

Validate a return

Check if a return can be announced **without** actually creating the return, or announcing it with the carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsValidate();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\V3\Model\ReturnValidation**](../Model/ReturnValidation.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
