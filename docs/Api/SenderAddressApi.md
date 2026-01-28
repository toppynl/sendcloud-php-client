# Toppy\Sendcloud\V3\SenderAddressApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3AddressesGetAllSenderAddresses()**](SenderAddressApi.md#scPublicV3AddressesGetAllSenderAddresses) | **GET** /addresses/sender-addresses | Retrieve a list of sender addresses
[**scPublicV3AddressesGetSenderAddressById()**](SenderAddressApi.md#scPublicV3AddressesGetSenderAddressById) | **GET** /addresses/sender-addresses/{id} | Retrieve a sender address


## `scPublicV3AddressesGetAllSenderAddresses()`

```php
scPublicV3AddressesGetAllSenderAddresses($cursor, $pageSize): \Toppy\Sendcloud\V3\Model\ScPublicV3AddressesGetAllSenderAddresses200Response
```

Retrieve a list of sender addresses

Returns a list of all the sender addresses which have been saved to your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\SenderAddressApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - `o`: Offset - `r`: Reverse - `p`: Position    For example, `r=1&p=300` encoded as a base64 string would be `cj0xJnA9MzAw`. The query string would then be `cursor=cj0xJnA9MzAw`.
$pageSize = 100; // int | The size of the page to fetch

try {
    $result = $apiInstance->scPublicV3AddressesGetAllSenderAddresses($cursor, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderAddressApi->scPublicV3AddressesGetAllSenderAddresses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - &#x60;o&#x60;: Offset - &#x60;r&#x60;: Reverse - &#x60;p&#x60;: Position    For example, &#x60;r&#x3D;1&amp;p&#x3D;300&#x60; encoded as a base64 string would be &#x60;cj0xJnA9MzAw&#x60;. The query string would then be &#x60;cursor&#x3D;cj0xJnA9MzAw&#x60;. | [optional]
 **pageSize** | **int**| The size of the page to fetch | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3AddressesGetAllSenderAddresses200Response**](../Model/ScPublicV3AddressesGetAllSenderAddresses200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3AddressesGetSenderAddressById()`

```php
scPublicV3AddressesGetSenderAddressById($id): \Toppy\Sendcloud\V3\Model\ScPublicV3AddressesGetSenderAddressById200Response
```

Retrieve a sender address

Retrieve information about a specific sender address saved to your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\SenderAddressApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1234; // int | The sender address unique identifier

try {
    $result = $apiInstance->scPublicV3AddressesGetSenderAddressById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderAddressApi->scPublicV3AddressesGetSenderAddressById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The sender address unique identifier |

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3AddressesGetSenderAddressById200Response**](../Model/ScPublicV3AddressesGetSenderAddressById200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
