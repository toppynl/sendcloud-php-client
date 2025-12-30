# Toppy\Sendcloud\FileUploadApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3DsfPostFiles()**](FileUploadApi.md#scPublicV3DsfPostFiles) | **POST** /dsf/files | Upload File


## `scPublicV3DsfPostFiles()`

```php
scPublicV3DsfPostFiles($file): \Toppy\Sendcloud\Model\ScPublicV3DsfPostFiles201Response
```

Upload File

API for uploading a file required for ticket creation.  The uploaded file is stored in the system, and a unique file token is returned in response.  The API is using rate limits.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\FileUploadApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$file = '/path/to/file.txt'; // \SplFileObject

try {
    $result = $apiInstance->scPublicV3DsfPostFiles($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileUploadApi->scPublicV3DsfPostFiles: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **\SplFileObject****\SplFileObject**|  |

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3DsfPostFiles201Response**](../Model/ScPublicV3DsfPostFiles201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
