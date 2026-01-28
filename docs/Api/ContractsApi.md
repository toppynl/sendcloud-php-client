# Toppy\Sendcloud\V3\ContractsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpDeleteContract()**](ContractsApi.md#scPublicV3ScpDeleteContract) | **DELETE** /contracts/{id} | Delete a contract
[**scPublicV3ScpGetAllContracts()**](ContractsApi.md#scPublicV3ScpGetAllContracts) | **GET** /contracts | Retrieve a list of contracts
[**scPublicV3ScpGetAllContractsSchemas()**](ContractsApi.md#scPublicV3ScpGetAllContractsSchemas) | **GET** /contracts/schemas | Retrieve a list of contract schemas
[**scPublicV3ScpGetSpecificContract()**](ContractsApi.md#scPublicV3ScpGetSpecificContract) | **GET** /contracts/{id} | Retrieve a contract
[**scPublicV3ScpPatchContract()**](ContractsApi.md#scPublicV3ScpPatchContract) | **PATCH** /contracts/{id} | Update a contract
[**scPublicV3ScpPostCreateContract()**](ContractsApi.md#scPublicV3ScpPostCreateContract) | **POST** /contracts | Create a contract for a carrier


## `scPublicV3ScpDeleteContract()`

```php
scPublicV3ScpDeleteContract($id)
```

Delete a contract

Delete a specific contract by including the `id` of the contract as a path parameter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The id of the contract.

try {
    $apiInstance->scPublicV3ScpDeleteContract($id);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpDeleteContract: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The id of the contract. |

### Return type

void (empty response body)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetAllContracts()`

```php
scPublicV3ScpGetAllContracts($carrierCode, $isActive, $clientId, $name, $countryCode, $cursor, $pageSize): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllContracts200Response
```

Retrieve a list of contracts

Retrieve the list of contracts you have in your Sendcloud account. It will also return the `id` of each contract, which you can use to retrieve information about a specific contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$carrierCode = 'carrierCode_example'; // string | The carrier you want to filter for, for instance: postnl. You can find available carriers in your Sendcloud account settings.
$isActive = True; // bool | Filter contracts based on the status.
$clientId = 'clientId_example'; // string | Filter direct contracts based on the client id.
$name = 'name_example'; // string | Filter direct contracts based on the contract's name. Will search for a case-sensitive exact match.
$countryCode = NL; // string | Filter contracts based on the country of the contract, it should be in the ISO 3166-1 alpha-2 format.
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - `o`: Offset - `r`: Reverse - `p`: Position    For example, `r=1&p=300` encoded as a base64 string would be `cj0xJnA9MzAw`. The query string would then be `cursor=cj0xJnA9MzAw`.
$pageSize = 100; // int | The size of the page to fetch

try {
    $result = $apiInstance->scPublicV3ScpGetAllContracts($carrierCode, $isActive, $clientId, $name, $countryCode, $cursor, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpGetAllContracts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrierCode** | **string**| The carrier you want to filter for, for instance: postnl. You can find available carriers in your Sendcloud account settings. | [optional]
 **isActive** | **bool**| Filter contracts based on the status. | [optional]
 **clientId** | **string**| Filter direct contracts based on the client id. | [optional]
 **name** | **string**| Filter direct contracts based on the contract&#39;s name. Will search for a case-sensitive exact match. | [optional]
 **countryCode** | **string**| Filter contracts based on the country of the contract, it should be in the ISO 3166-1 alpha-2 format. | [optional]
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - &#x60;o&#x60;: Offset - &#x60;r&#x60;: Reverse - &#x60;p&#x60;: Position    For example, &#x60;r&#x3D;1&amp;p&#x3D;300&#x60; encoded as a base64 string would be &#x60;cj0xJnA9MzAw&#x60;. The query string would then be &#x60;cursor&#x3D;cj0xJnA9MzAw&#x60;. | [optional]
 **pageSize** | **int**| The size of the page to fetch | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllContracts200Response**](../Model/ScPublicV3ScpGetAllContracts200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetAllContractsSchemas()`

```php
scPublicV3ScpGetAllContractsSchemas($carrierCode): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllContractsSchemas200Response
```

Retrieve a list of contract schemas

Retrieve information about contract schemas (by carrier) to help with creating/updating contracts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$carrierCode = postnl; // string | The carrier you want to filter for, for instance: postnl. You can find available carriers in your Sendcloud account settings.

try {
    $result = $apiInstance->scPublicV3ScpGetAllContractsSchemas($carrierCode);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpGetAllContractsSchemas: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **carrierCode** | **string**| The carrier you want to filter for, for instance: postnl. You can find available carriers in your Sendcloud account settings. | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllContractsSchemas200Response**](../Model/ScPublicV3ScpGetAllContractsSchemas200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetSpecificContract()`

```php
scPublicV3ScpGetSpecificContract($id): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetSpecificContract200Response
```

Retrieve a contract

Retrieve information about a specific contract by including the `id` of the contract as a path parameter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The id of the contract.

try {
    $result = $apiInstance->scPublicV3ScpGetSpecificContract($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpGetSpecificContract: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The id of the contract. |

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetSpecificContract200Response**](../Model/ScPublicV3ScpGetSpecificContract200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPatchContract()`

```php
scPublicV3ScpPatchContract($id, $updateContractRequest): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPatchContract200Response
```

Update a contract

Update or replace a contract by including the `id` of the contract as a path parameter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The id of the contract.
$updateContractRequest = new \Toppy\Sendcloud\V3\Model\UpdateContractRequest(); // \Toppy\Sendcloud\V3\Model\UpdateContractRequest

try {
    $result = $apiInstance->scPublicV3ScpPatchContract($id, $updateContractRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpPatchContract: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The id of the contract. |
 **updateContractRequest** | [**\Toppy\Sendcloud\V3\Model\UpdateContractRequest**](../Model/UpdateContractRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPatchContract200Response**](../Model/ScPublicV3ScpPatchContract200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCreateContract()`

```php
scPublicV3ScpPostCreateContract($createContractRequest): \Toppy\Sendcloud\V3\Model\ContractCreatedResponse
```

Create a contract for a carrier

Create a contract for a supported carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$createContractRequest = new \Toppy\Sendcloud\V3\Model\CreateContractRequest(); // \Toppy\Sendcloud\V3\Model\CreateContractRequest

try {
    $result = $apiInstance->scPublicV3ScpPostCreateContract($createContractRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractsApi->scPublicV3ScpPostCreateContract: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createContractRequest** | [**\Toppy\Sendcloud\V3\Model\CreateContractRequest**](../Model/CreateContractRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ContractCreatedResponse**](../Model/ContractCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
