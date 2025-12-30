# Toppy\Sendcloud\ParcelStatusesApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetAllParcelStatuses()**](ParcelStatusesApi.md#scPublicV3ScpGetAllParcelStatuses) | **GET** /parcels/statuses | Retrieve a list of all possible parcel statuses


## `scPublicV3ScpGetAllParcelStatuses()`

```php
scPublicV3ScpGetAllParcelStatuses(): \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllParcelStatuses200Response
```

Retrieve a list of all possible parcel statuses

This endpoint will retrieve information about all possible Parcel Statuses

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ParcelStatusesApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3ScpGetAllParcelStatuses();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ParcelStatusesApi->scPublicV3ScpGetAllParcelStatuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllParcelStatuses200Response**](../Model/ScPublicV3ScpGetAllParcelStatuses200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
