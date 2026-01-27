# Toppy\Sendcloud\ReturnsApi

All URIs are relative to https://account.sendcloud.com.

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
scPublicV3ScpGetReturnsGetDetails($id): \Toppy\Sendcloud\Model\ModelReturn
```

Retrieve a return

Retrieve information about a specific return parcel based on the return `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
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

[**\Toppy\Sendcloud\Model\ModelReturn**](../Model/ModelReturn.md)

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
scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $cursor, $parentParcelStatus, $pageSize): \Toppy\Sendcloud\Model\ScPublicV3ScpGetReturnsGetReturns200Response
```

Retrieve a list of returns

Retrieve a list of returns which have been created under your API credentials.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$fromDate = 2022-04-06 00:00:00; // string | Excludes all returns before this datetime
$toDate = 2022-04-07 00:00:00; // string | Excludes all returns after this datetime
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - `o`: Offset - `r`: Reverse - `p`: Position    For example, `r=1&p=300` encoded as a base64 string would be `cj0xJnA9MzAw`. The query string would then be `cursor=cj0xJnA9MzAw`.
$parentParcelStatus = announced; // string | Search for returns with this parent status
$pageSize = 10; // float | Refers to the number of items per page

try {
    $result = $apiInstance->scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $cursor, $parentParcelStatus, $pageSize);
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
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - &#x60;o&#x60;: Offset - &#x60;r&#x60;: Reverse - &#x60;p&#x60;: Position    For example, &#x60;r&#x3D;1&amp;p&#x3D;300&#x60; encoded as a base64 string would be &#x60;cj0xJnA9MzAw&#x60;. The query string would then be &#x60;cursor&#x3D;cj0xJnA9MzAw&#x60;. | [optional]
 **parentParcelStatus** | **string**| Search for returns with this parent status | [optional]
 **pageSize** | **float**| Refers to the number of items per page | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetReturnsGetReturns200Response**](../Model/ScPublicV3ScpGetReturnsGetReturns200Response.md)

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
scPublicV3ScpPatchReturnsCancel($id): \Toppy\Sendcloud\Model\ScPublicV3ScpPatchReturnsCancel202Response
```

Request cancellation of a return

You can request cancellation for a return by providing the return `id` to this endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPatchReturnsCancel202Response**](../Model/ScPublicV3ScpPatchReturnsCancel202Response.md)

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
scPublicV3ScpPostReturnsCreateNewReturn($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return

Create a standalone return

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturn($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturn: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsCreateNewReturnSynchronously()`

```php
scPublicV3ScpPostReturnsCreateNewReturnSynchronously($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return synchronously

Create a return synchronously, i.e. wait for a response from the carrier before continuing.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturnSynchronously($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturnSynchronously: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsValidate()`

```php
scPublicV3ScpPostReturnsValidate($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ReturnValidation
```

Validate a return

Check if a return can be announced **without** actually creating the return, or announcing it with the carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsValidate($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ReturnValidation**](../Model/ReturnValidation.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
