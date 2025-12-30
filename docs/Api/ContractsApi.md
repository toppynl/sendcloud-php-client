# Toppy\Sendcloud\ContractsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpDeleteContract()**](ContractsApi.md#scPublicV3ScpDeleteContract) | **DELETE** /contracts/{id} | Delete a contract
[**scPublicV3ScpGetAllContracts()**](ContractsApi.md#scPublicV3ScpGetAllContracts) | **GET** /contracts | Retrieve a list of contracts
[**scPublicV3ScpGetAllContractsSchemas()**](ContractsApi.md#scPublicV3ScpGetAllContractsSchemas) | **GET** /contracts/schemas | Retrieve a list of contracts schemas
[**scPublicV3ScpGetSpecificContract()**](ContractsApi.md#scPublicV3ScpGetSpecificContract) | **GET** /contracts/{id} | Retrieve a contract
[**scPublicV3ScpPatchContract()**](ContractsApi.md#scPublicV3ScpPatchContract) | **PATCH** /contracts/{id} | Update a contract
[**scPublicV3ScpPostCreateContract()**](ContractsApi.md#scPublicV3ScpPostCreateContract) | **POST** /contracts | Create a contract for carrier


## `scPublicV3ScpDeleteContract()`

```php
scPublicV3ScpDeleteContract($id)
```

Delete a contract

This endpoint **deletes** a contract.  Include the `id` of the Contract for a specific direct contract as a path parameter to delete information for this specific contract.  If you have multiple active contracts for the same carrier and you delete the default contract, we will automatically pick the first added contract as the new default.  If you delete the last contract for a specific carrier, we will disable this carrier and it's shipping options to prevent that you will accidentally use Sendcloud's transactional rates.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
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
scPublicV3ScpGetAllContracts($carrierCode, $isActive, $clientId, $name, $countryCode, $cursor, $pageSize): \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllContracts200Response
```

Retrieve a list of contracts

This endpoint will retrieve information about all of the available contracts you have in your Sendcloud account. It will also return the `id` of the Contract of your contracts, which you can use to retrieve information about a specific contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
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
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - `o`: Offset     - `r`: Reverse     - `p`: Position   Combine into GET parameters, for example: `r=1&p=300`   Base 64 encoded it would become: `cj0xJnA9MzAw`   GET parameter in URL would be `https://some.url.com/api/endpoint/?cursor=cj0xJnA9MzAw`
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
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - &#x60;o&#x60;: Offset     - &#x60;r&#x60;: Reverse     - &#x60;p&#x60;: Position   Combine into GET parameters, for example: &#x60;r&#x3D;1&amp;p&#x3D;300&#x60;   Base 64 encoded it would become: &#x60;cj0xJnA9MzAw&#x60;   GET parameter in URL would be &#x60;https://some.url.com/api/endpoint/?cursor&#x3D;cj0xJnA9MzAw&#x60; | [optional]
 **pageSize** | **int**| The size of the page to fetch | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllContracts200Response**](../Model/ScPublicV3ScpGetAllContracts200Response.md)

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
scPublicV3ScpGetAllContractsSchemas($carrierCode): \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllContractsSchemas200Response
```

Retrieve a list of contracts schemas

This endpoint will retrieve information about all schemas for creating/updating contracts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllContractsSchemas200Response**](../Model/ScPublicV3ScpGetAllContractsSchemas200Response.md)

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
scPublicV3ScpGetSpecificContract($id): \Toppy\Sendcloud\Model\ScPublicV3ScpGetSpecificContract200Response
```

Retrieve a contract

Include the `id` of the Contract for a specific direct contract as a path parameter to retrieve information for this specific contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetSpecificContract200Response**](../Model/ScPublicV3ScpGetSpecificContract200Response.md)

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
scPublicV3ScpPatchContract($id, $updateContractRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpPatchContract200Response
```

Update a contract

This endpoint **updates** a contract.  This endpoint will either update or replace the contract. Changes to unused contracts or the contract's state  and description will be done in place and not cause a new contract to be created (name, is_active, is_default, is_per_carrier_default).  **However, used contracts are immutable, if you change the contract_data of a contract that has already been used for shipments,  it will cause a new contract ID to be created. In this case, the old one will no longer be active for use.**  After updating a contract with contract_data, we need to validate it again and its state will be `\"validating\"`. During the validation the contract is not active and can not be used for creating shipments. The validation process is asynchronous and will happen in the background.  Once validation is complete, the contract's state will change to one of the following:  - `\"active\"` or `\"inactive\"`: The contract has been successfully processed.   - `\"validation_failed\"`: An error occurred during validation. Additional information about the failure will be provided.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The id of the contract.
$updateContractRequest = new \Toppy\Sendcloud\Model\UpdateContractRequest(); // \Toppy\Sendcloud\Model\UpdateContractRequest

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
 **updateContractRequest** | [**\Toppy\Sendcloud\Model\UpdateContractRequest**](../Model/UpdateContractRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPatchContract200Response**](../Model/ScPublicV3ScpPatchContract200Response.md)

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
scPublicV3ScpPostCreateContract($createContractRequest): \Toppy\Sendcloud\Model\ContractCreatedResponse
```

Create a contract for carrier

This endpoint **creates** a contract.  <!-- theme: warning --> >**Creating a carrier contract via the API is not supported for 2FA carriers, including UPS, Hermes, Amazon, Bol, and FedEx. To create a carrier contract for these carriers, please use the Sendcloud Panel.**  After creating a contract, its initial state will be `\"validating\"`. This means the system is verifying the contract data with carriers, which typically takes only a few seconds, depending on the carriers.    Once validation is complete, the contract's state will change to one of the following:  - `\"active\"` or `\"inactive\"`: The contract has been successfully processed.   - `\"validation_failed\"`: An error occurred during validation. Additional information about the failure will be provided.    You can check the current state of the contract using the **Retrieve a contract** endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ContractsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$createContractRequest = new \Toppy\Sendcloud\Model\CreateContractRequest(); // \Toppy\Sendcloud\Model\CreateContractRequest

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
 **createContractRequest** | [**\Toppy\Sendcloud\Model\CreateContractRequest**](../Model/CreateContractRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ContractCreatedResponse**](../Model/ContractCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
