# Toppy\Sendcloud\V3\UserApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetUserAuthMetadata()**](UserApi.md#scPublicV3ScpGetUserAuthMetadata) | **GET** /user/auth/metadata | Retrieve metadata associated with the authentication method


## `scPublicV3ScpGetUserAuthMetadata()`

```php
scPublicV3ScpGetUserAuthMetadata(): \Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetUserAuthMetadata200Response
```

Retrieve metadata associated with the authentication method

Retrieve information about the metadata associated with the authentication method used in the request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\UserApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3ScpGetUserAuthMetadata();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->scPublicV3ScpGetUserAuthMetadata: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3ScpGetUserAuthMetadata200Response**](../Model/ScPublicV3ScpGetUserAuthMetadata200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
