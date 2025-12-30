# Toppy\Sendcloud\PickupsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetAllPickups()**](PickupsApi.md#scPublicV3ScpGetAllPickups) | **GET** /pickups | Retrieve a list of pickups
[**scPublicV3ScpGetPickup()**](PickupsApi.md#scPublicV3ScpGetPickup) | **GET** /pickups/{id} | Retrieve a pickup
[**scPublicV3ScpPostPickup()**](PickupsApi.md#scPublicV3ScpPostPickup) | **POST** /pickups | Create a pickup


## `scPublicV3ScpGetAllPickups()`

```php
scPublicV3ScpGetAllPickups($pageSize): \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllPickups200Response
```

Retrieve a list of pickups

This endpoint retrieves information about all the pickups which have been created from your account. This is limited to the carriers which support pickups via the API. The response includes information about when the pickup was scheduled, the latest status, the parcel tracking number and the time frame in which the pickup is due to take place.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\PickupsApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllPickups200Response**](../Model/ScPublicV3ScpGetAllPickups200Response.md)

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
scPublicV3ScpGetPickup($id): \Toppy\Sendcloud\Model\ScPublicV3ScpGetPickup200Response
```

Retrieve a pickup

This endpoint allows you to retrieve information about a specific pickup based on the pickup `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\PickupsApi(
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

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetPickup200Response**](../Model/ScPublicV3ScpGetPickup200Response.md)

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
scPublicV3ScpPostPickup($scPublicV3ScpPostPickupRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpGetPickup200Response
```

Create a pickup

This endpoint allows you to schedule a pickup with a [**supporting carrier**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/pickups#which-carriers-support-pickups-via-the-api). Schedule a pickup time and choose a location, and include any additional instructions to the driver by including the `special_instructions` parameter. When a pickup is successfully scheduled a pickup `id` will be returned.  <!-- theme: warning --> > If you have more than one added active contracts for specific carrier, you must fill `contract` attribute with your desired contract's ID in your request. You can get your contracts ID from [**Retrieve a list of contracts**](https://api.sendcloud.dev/docs/sendcloud-public-api/contracts/operations/list-contracts).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\PickupsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3ScpPostPickupRequest = {"address":{"name":"John Doe","company_name":"Sendcloud","country_code":"NL","city":"Eindhoven","email":"example@sendcloud.com","address_line_1":"Stadhuisplein","house_number":"10","address_line_2":"","postal_code":"5611 EM","phone_number":"+310612345678"},"time_slots":[{"start_at":"2022-04-06T12:00:00Z","end_at":"2022-04-06T17:00:00Z"}],"items":[{"quantity":20,"container_type":"parcel","total_weight":{"value":"1.00","unit":"kg"}}],"carrier_code":"dhl_express"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostPickupRequest | 

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
 **scPublicV3ScpPostPickupRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostPickupRequest**](../Model/ScPublicV3ScpPostPickupRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetPickup200Response**](../Model/ScPublicV3ScpGetPickup200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
