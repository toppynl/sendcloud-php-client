# Toppy\Sendcloud\ParcelDocumentsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetRetrieveParcelDocuments()**](ParcelDocumentsApi.md#scPublicV3ScpGetRetrieveParcelDocuments) | **GET** /parcels/{id}/documents/{type} | Retrieve a parcel document
[**scPublicV3ScpGetRetrieveParcelDocumentsBulk()**](ParcelDocumentsApi.md#scPublicV3ScpGetRetrieveParcelDocumentsBulk) | **GET** /parcel-documents/{type} | Retrieve multiple parcel documents


## `scPublicV3ScpGetRetrieveParcelDocuments()`

```php
scPublicV3ScpGetRetrieveParcelDocuments($id, $type, $dpi, $accept, $paperSize): \SplFileObject
```

Retrieve a parcel document

For international shipments, customs declaration must be attached (either physically or [**digitally**](https://support.sendcloud.com/hc/en-us/articles/4417349714452-Send-your-customs-documents-digitally-via-Paperless-Trade-) for some carriers) to the shipment for customs officials to access.  Sendcloud generates the correct type of document for your shipment when you [**Create a parcel**](https://api.sendcloud.dev/docs/sendcloud-public-api/parcels/operations/create-a-parcel), provided that you have filled in all the information related to the parcel contents, value and invoice. Use this endpoint to retrieve these documents in your preferred format.   The endpoint supports the following document types:  - `label` - `customs-declaration` - `air-waybill`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ParcelDocumentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1; // int | Identifier of the parcel which you want to retrieve a document from
$type = customs-declaration; // string | Document type you want to retrieve.
$dpi = 300; // int | DPI refers to the printing resolution of your shipping labels. Labels must be printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes. Use following amounts for appropriate result: <table>   <thead>     <tr>       <th>File format</th>       <th>Default DPI</th>       <th>Valid DPI</th>     </tr>   </thead>   <tbody>     <tr>       <td>pdf</td>       <td>72</td>       <td>72</td>     </tr>     <tr>       <td>png</td>       <td>300</td>       <td>150, 300</td>     </tr>   </tbody> </table> ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities.
$accept = image/png; // string | The returned format of the document. **Note**: If a label is requested as native ZPL from the carrier it can't be converted to another format and will always be returned in ZPL.
$paperSize = A4; // string | The paper size of the document you would like to retrieve. Paper size can be one of:   - A4   - A5   - A6 Omitting this query parameter leads to the internal paper size of the document being used, generally this is A6 for labels and A4 for larger documents, like customs documents.

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
 **dpi** | **int**| DPI refers to the printing resolution of your shipping labels. Labels must be printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes. Use following amounts for appropriate result: &lt;table&gt;   &lt;thead&gt;     &lt;tr&gt;       &lt;th&gt;File format&lt;/th&gt;       &lt;th&gt;Default DPI&lt;/th&gt;       &lt;th&gt;Valid DPI&lt;/th&gt;     &lt;/tr&gt;   &lt;/thead&gt;   &lt;tbody&gt;     &lt;tr&gt;       &lt;td&gt;pdf&lt;/td&gt;       &lt;td&gt;72&lt;/td&gt;       &lt;td&gt;72&lt;/td&gt;     &lt;/tr&gt;     &lt;tr&gt;       &lt;td&gt;png&lt;/td&gt;       &lt;td&gt;300&lt;/td&gt;       &lt;td&gt;150, 300&lt;/td&gt;     &lt;/tr&gt;   &lt;/tbody&gt; &lt;/table&gt; ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities. | [optional] [default to 72]
 **accept** | **string**| The returned format of the document. **Note**: If a label is requested as native ZPL from the carrier it can&#39;t be converted to another format and will always be returned in ZPL. | [optional] [default to &#39;application/pdf&#39;]
 **paperSize** | **string**| The paper size of the document you would like to retrieve. Paper size can be one of:   - A4   - A5   - A6 Omitting this query parameter leads to the internal paper size of the document being used, generally this is A6 for labels and A4 for larger documents, like customs documents. | [optional]

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
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ParcelDocumentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$parcels = ["1,2,3"]; // int[] | Parcels for which you want to retrieve the documents
$type = customs-declaration; // string | Document type you want to retrieve.
$paperSize = A4; // string | The paper size of the document you would like to retrieve. Paper size can be one of:   - A4   - A5   - A6 Omitting this query parameter leads to the internal paper size of the document being used, generally this is A6 for labels and A4 for larger documents, like customs documents.

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
 **paperSize** | **string**| The paper size of the document you would like to retrieve. Paper size can be one of:   - A4   - A5   - A6 Omitting this query parameter leads to the internal paper size of the document being used, generally this is A6 for labels and A4 for larger documents, like customs documents. | [optional]

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
