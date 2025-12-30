# Toppy\Sendcloud\CarrierSupportContactsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3DsfDeleteCarrierSupportContacts()**](CarrierSupportContactsApi.md#scPublicV3DsfDeleteCarrierSupportContacts) | **DELETE** /dsf/carrier-support-contacts/{id} | Delete carrier support contact
[**scPublicV3DsfGetCarrierSupportContacts()**](CarrierSupportContactsApi.md#scPublicV3DsfGetCarrierSupportContacts) | **GET** /dsf/carrier-support-contacts | Get carrier support contacts
[**scPublicV3DsfPatchCarrierSupportContacts()**](CarrierSupportContactsApi.md#scPublicV3DsfPatchCarrierSupportContacts) | **PATCH** /dsf/carrier-support-contacts/{id} | Update carrier support contact
[**scPublicV3DsfPostCarrierSupportContacts()**](CarrierSupportContactsApi.md#scPublicV3DsfPostCarrierSupportContacts) | **POST** /dsf/carrier-support-contacts | Create carrier support contact


## `scPublicV3DsfDeleteCarrierSupportContacts()`

```php
scPublicV3DsfDeleteCarrierSupportContacts($id)
```

Delete carrier support contact

API for deleting existing carrier support contacts.  A carrier support contact is required in order to create tickets for shipments sent under your own carrier contract. By providing this information, we know where to forward the claim.  Ticket creation will fail if a carrier support contact is missing for a carrier you use with your own contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CarrierSupportContactsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Support contact id

try {
    $apiInstance->scPublicV3DsfDeleteCarrierSupportContacts($id);
} catch (Exception $e) {
    echo 'Exception when calling CarrierSupportContactsApi->scPublicV3DsfDeleteCarrierSupportContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Support contact id |

### Return type

void (empty response body)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfGetCarrierSupportContacts()`

```php
scPublicV3DsfGetCarrierSupportContacts(): \Toppy\Sendcloud\Model\CarrierSupportContact
```

Get carrier support contacts

API for retrieving carrier support contacts.  A carrier support contact is required in order to create tickets for shipments sent under your own carrier contract. By providing this information, we know where to forward the claim.  Ticket creation will fail if a carrier support contact is missing for a carrier you use with your own contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CarrierSupportContactsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3DsfGetCarrierSupportContacts();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarrierSupportContactsApi->scPublicV3DsfGetCarrierSupportContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\Model\CarrierSupportContact**](../Model/CarrierSupportContact.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPatchCarrierSupportContacts()`

```php
scPublicV3DsfPatchCarrierSupportContacts($id, $patchSupportContactRequest): \Toppy\Sendcloud\Model\CarrierSupportContact
```

Update carrier support contact

API for updating existing carrier support contacts.  A carrier support contact is required in order to create tickets for shipments sent under your own carrier contract. By providing this information, we know where to forward the claim.  Ticket creation will fail if a carrier support contact is missing for a carrier you use with your own contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CarrierSupportContactsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Support contact id
$patchSupportContactRequest = new \Toppy\Sendcloud\Model\PatchSupportContactRequest(); // \Toppy\Sendcloud\Model\PatchSupportContactRequest

try {
    $result = $apiInstance->scPublicV3DsfPatchCarrierSupportContacts($id, $patchSupportContactRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarrierSupportContactsApi->scPublicV3DsfPatchCarrierSupportContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Support contact id |
 **patchSupportContactRequest** | [**\Toppy\Sendcloud\Model\PatchSupportContactRequest**](../Model/PatchSupportContactRequest.md)|  |

### Return type

[**\Toppy\Sendcloud\Model\CarrierSupportContact**](../Model/CarrierSupportContact.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostCarrierSupportContacts()`

```php
scPublicV3DsfPostCarrierSupportContacts($createSupportContactRequest): \Toppy\Sendcloud\Model\CarrierSupportContact
```

Create carrier support contact

API for creating carrier support contacts.  A carrier support contact is required in order to create tickets for shipments sent under your own carrier contract. By providing this information, we know where to forward the claim.  Ticket creation will fail if a carrier support contact is missing for a carrier you use with your own contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\CarrierSupportContactsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$createSupportContactRequest = new \Toppy\Sendcloud\Model\CreateSupportContactRequest(); // \Toppy\Sendcloud\Model\CreateSupportContactRequest

try {
    $result = $apiInstance->scPublicV3DsfPostCarrierSupportContacts($createSupportContactRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarrierSupportContactsApi->scPublicV3DsfPostCarrierSupportContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createSupportContactRequest** | [**\Toppy\Sendcloud\Model\CreateSupportContactRequest**](../Model/CreateSupportContactRequest.md)|  |

### Return type

[**\Toppy\Sendcloud\Model\CarrierSupportContact**](../Model/CarrierSupportContact.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
