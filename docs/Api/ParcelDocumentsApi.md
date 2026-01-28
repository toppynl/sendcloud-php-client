# Toppy\Sendcloud\V3\ParcelDocumentsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetRetrieveParcelDocuments()**](ParcelDocumentsApi.md#scPublicV3ScpGetRetrieveParcelDocuments) | **GET** /parcels/{id}/documents/{type} | Retrieve a parcel document
[**scPublicV3ScpGetRetrieveParcelDocumentsBulk()**](ParcelDocumentsApi.md#scPublicV3ScpGetRetrieveParcelDocumentsBulk) | **GET** /parcel-documents/{type} | Retrieve multiple parcel documents


## `scPublicV3ScpGetRetrieveParcelDocuments()`

```php
scPublicV3ScpGetRetrieveParcelDocuments($id, $type, $dpi, $accept, $paperSize): \SplFileObject
```

Retrieve a parcel document

Retrieve a specific document for a given parcel, and download it in your preferred format and resolution.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ParcelDocumentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1; // int | Identifier of the parcel which you want to retrieve a document from
$type = customs-declaration; // string | Document type you want to retrieve.
$dpi = 300; // int | DPI, or dots per inch, refers to the printing resolution of your shipping labels. Labels must be printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes.  Use the following table to find the appropriate DPI for each file format:  | File format | Default DPI | Valid DPI | |-------------|-------------|-----------| | pdf         | 72          | 72        | | png         | 300         | 150, 300  |  ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities.
$accept = image/png; // string | The returned format of the document.  **Note:** If a label is requested as native ZPL from the carrier it can't be converted to another format and will always be returned in ZPL.
$paperSize = A4; // string | The paper size of the document you would like to retrieve. Paper size can be one of:  - A4 - A5 - A6  Omitting this query parameter leads to the internal paper size of the document being used. Generally this is A6 for labels and A4 for larger documents, like customs documents.

try {
    $result = $apiInstance->scPublicV3ScpGetRetrieveParcelDocuments($id, $type, $dpi, $accept, $paperSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ParcelDocumentsApi->scPublicV3ScpGetRetrieveParcelDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Identifier of the parcel which you want to retrieve a document from |
 **type** | **string**| Document type you want to retrieve. |
 **dpi** | **int**| DPI, or dots per inch, refers to the printing resolution of your shipping labels. Labels must be printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes.  Use the following table to find the appropriate DPI for each file format:  | File format | Default DPI | Valid DPI | |-------------|-------------|-----------| | pdf         | 72          | 72        | | png         | 300         | 150, 300  |  ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities. | [optional] [default to 72]
 **accept** | **string**| The returned format of the document.  **Note:** If a label is requested as native ZPL from the carrier it can&#39;t be converted to another format and will always be returned in ZPL. | [optional] [default to &#39;application/pdf&#39;]
 **paperSize** | **string**| The paper size of the document you would like to retrieve. Paper size can be one of:  - A4 - A5 - A6  Omitting this query parameter leads to the internal paper size of the document being used. Generally this is A6 for labels and A4 for larger documents, like customs documents. | [optional]

### Return type

**\SplFileObject**

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/zpl`, `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetRetrieveParcelDocumentsBulk()`

```php
scPublicV3ScpGetRetrieveParcelDocumentsBulk($parcels, $type, $paperSize): \SplFileObject
```

Retrieve multiple parcel documents

Download multiple parcel documents of the same type in bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\ParcelDocumentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$parcels = [1,2,3]; // int[] | Parcels for which you want to retrieve the documents
$type = customs-declaration; // string | Document type you want to retrieve.
$paperSize = A4; // string | The paper size of the document you would like to retrieve. Paper size can be one of:  - A4 - A5 - A6  Omitting this query parameter leads to the internal paper size of the document being used. Generally this is A6 for labels and A4 for larger documents, like customs documents.

try {
    $result = $apiInstance->scPublicV3ScpGetRetrieveParcelDocumentsBulk($parcels, $type, $paperSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ParcelDocumentsApi->scPublicV3ScpGetRetrieveParcelDocumentsBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parcels** | [**int[]**](../Model/int.md)| Parcels for which you want to retrieve the documents |
 **type** | **string**| Document type you want to retrieve. |
 **paperSize** | **string**| The paper size of the document you would like to retrieve. Paper size can be one of:  - A4 - A5 - A6  Omitting this query parameter leads to the internal paper size of the document being used. Generally this is A6 for labels and A4 for larger documents, like customs documents. | [optional]

### Return type

**\SplFileObject**

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/zpl`, `image/png`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
