# Toppy\Sendcloud\SenderAddressApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3AddressesGetAllSenderAddresses()**](SenderAddressApi.md#scPublicV3AddressesGetAllSenderAddresses) | **GET** /addresses/sender-addresses | Retrieve a list of sender addresses
[**scPublicV3AddressesGetSenderAddressById()**](SenderAddressApi.md#scPublicV3AddressesGetSenderAddressById) | **GET** /addresses/sender-addresses/{id} | Retrieve a sender address


## `scPublicV3AddressesGetAllSenderAddresses()`

```php
scPublicV3AddressesGetAllSenderAddresses($cursor, $pageSize): \Toppy\Sendcloud\Model\ScPublicV3AddressesGetAllSenderAddresses200Response
```

Retrieve a list of sender addresses

This endpoint returns a list of all the sender addresses which have been saved to your account. The response will include the `id` of each address.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\SenderAddressApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - `o`: Offset     - `r`: Reverse     - `p`: Position   Combine into GET parameters, for example: `r=1&p=300`   Base 64 encoded it would become: `cj0xJnA9MzAw`   GET parameter in URL would be `https://some.url.com/api/endpoint/?cursor=cj0xJnA9MzAw`
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
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - &#x60;o&#x60;: Offset     - &#x60;r&#x60;: Reverse     - &#x60;p&#x60;: Position   Combine into GET parameters, for example: &#x60;r&#x3D;1&amp;p&#x3D;300&#x60;   Base 64 encoded it would become: &#x60;cj0xJnA9MzAw&#x60;   GET parameter in URL would be &#x60;https://some.url.com/api/endpoint/?cursor&#x3D;cj0xJnA9MzAw&#x60; | [optional]
 **pageSize** | **int**| The size of the page to fetch | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3AddressesGetAllSenderAddresses200Response**](../Model/ScPublicV3AddressesGetAllSenderAddresses200Response.md)

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
scPublicV3AddressesGetSenderAddressById($id): \Toppy\Sendcloud\Model\ScPublicV3AddressesGetSenderAddressById200Response
```

Retrieve a sender address

You can retrieve information about a specific sender address saved to your account via this endpoint. Sender address `id` can be obtained via the [**Get sender address**](https://api.sendcloud.dev/docs/sendcloud-public-api/sender-addresses/operations/get-a-user-address-sender) endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\SenderAddressApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3AddressesGetSenderAddressById200Response**](../Model/ScPublicV3AddressesGetSenderAddressById200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
