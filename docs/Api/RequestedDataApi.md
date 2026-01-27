# Toppy\Sendcloud\RequestedDataApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3DsfGetRequestedData()**](RequestedDataApi.md#scPublicV3DsfGetRequestedData) | **GET** /support/dsf/tickets/requested-data | Retrieve requested data for open tickets
[**scPublicV3DsfPostRequestedData()**](RequestedDataApi.md#scPublicV3DsfPostRequestedData) | **POST** /support/dsf/tickets/requested-data | Provide requested data


## `scPublicV3DsfGetRequestedData()`

```php
scPublicV3DsfGetRequestedData(): \Toppy\Sendcloud\Model\ScPublicV3DsfGetRequestedData200Response
```

Retrieve requested data for open tickets

Retrieve the list of additional data requests for open tickets handled by Support Automation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\RequestedDataApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3DsfGetRequestedData();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RequestedDataApi->scPublicV3DsfGetRequestedData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3DsfGetRequestedData200Response**](../Model/ScPublicV3DsfGetRequestedData200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3DsfPostRequestedData()`

```php
scPublicV3DsfPostRequestedData($scPublicV3DsfPostRequestedDataRequest)
```

Provide requested data

Depending on the requested `data_type`, additional documents/photos, text input, or sales data may be required.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\RequestedDataApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3DsfPostRequestedDataRequest = {"request_id":144,"comment":"Sales invoice","attachments":[{"file_token":"4b08344f-8325-40df-8273-c0c31c412bb0"}]}; // \Toppy\Sendcloud\Model\ScPublicV3DsfPostRequestedDataRequest

try {
    $apiInstance->scPublicV3DsfPostRequestedData($scPublicV3DsfPostRequestedDataRequest);
} catch (Exception $e) {
    echo 'Exception when calling RequestedDataApi->scPublicV3DsfPostRequestedData: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3DsfPostRequestedDataRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3DsfPostRequestedDataRequest**](../Model/ScPublicV3DsfPostRequestedDataRequest.md)|  |

### Return type

void (empty response body)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
