# Toppy\Sendcloud\V3\PickupsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetAllPickups()**](PickupsApi.md#scPublicV3ScpGetAllPickups) | **GET** /pickups | Retrieve a list of pickups
[**scPublicV3ScpGetPickup()**](PickupsApi.md#scPublicV3ScpGetPickup) | **GET** /pickups/{id} | Retrieve a pickup
[**scPublicV3ScpPostPickup()**](PickupsApi.md#scPublicV3ScpPostPickup) | **POST** /pickups | Create a pickup


## `scPublicV3ScpGetAllPickups()`

```php
scPublicV3ScpGetAllPickups($pageSize): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllPickups200Response
```

Retrieve a list of pickups

Get information about all the pickups which have been created from your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\PickupsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$pageSize = 10; // int | Amount of pickups that will be shown per page.

try {
    $result = $apiInstance->scPublicV3ScpGetAllPickups($pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PickupsApi->scPublicV3ScpGetAllPickups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pageSize** | **int**| Amount of pickups that will be shown per page. | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetAllPickups200Response**](../Model/ScPublicV3ScpGetAllPickups200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetPickup()`

```php
scPublicV3ScpGetPickup($id): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetPickup200Response
```

Retrieve a pickup

Retrieve information about a specific pickup based on the pickup `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\PickupsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | The `id` of the pickup you want to retrieve.

try {
    $result = $apiInstance->scPublicV3ScpGetPickup($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PickupsApi->scPublicV3ScpGetPickup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The &#x60;id&#x60; of the pickup you want to retrieve. |

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetPickup200Response**](../Model/ScPublicV3ScpGetPickup200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostPickup()`

```php
scPublicV3ScpPostPickup($scPublicV3ScpPostPickupRequest): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetPickup200Response
```

Create a pickup

Schedule a one-time pickup with a supported carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\PickupsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3ScpPostPickupRequest = {"address":{"name":"John Doe","company_name":"Sendcloud","country_code":"NL","city":"Eindhoven","email":"example@sendcloud.com","address_line_1":"Stadhuisplein","house_number":"10","address_line_2":"","postal_code":"5611 EM","phone_number":"+310612345678"},"time_slots":[{"start_at":"2022-04-06T12:00:00Z","end_at":"2022-04-06T17:00:00Z"}],"items":[{"quantity":20,"container_type":"parcel","total_weight":{"value":"1.00","unit":"kg"}}],"carrier_code":"dhl_express"}; // \Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostPickupRequest | 

try {
    $result = $apiInstance->scPublicV3ScpPostPickup($scPublicV3ScpPostPickupRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PickupsApi->scPublicV3ScpPostPickup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3ScpPostPickupRequest** | [**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpPostPickupRequest**](../Model/ScPublicV3ScpPostPickupRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetPickup200Response**](../Model/ScPublicV3ScpGetPickup200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
