# Toppy\Sendcloud\RequestedDataApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3DsfGetRequestedData()**](RequestedDataApi.md#scPublicV3DsfGetRequestedData) | **GET** /support/dsf/tickets/requested-data | Retrieve requested data.
[**scPublicV3DsfPostRequestedData()**](RequestedDataApi.md#scPublicV3DsfPostRequestedData) | **POST** /support/dsf/tickets/requested-data | Provide a requested data.


## `scPublicV3DsfGetRequestedData()`

```php
scPublicV3DsfGetRequestedData(): \Toppy\Sendcloud\Model\ScPublicV3DsfGetRequestedData200Response
```

Retrieve requested data.

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

Provide a requested data.

Endpoint to submit requested data.  Depending on the requested `data_type`, additional documents/photos, text input, or sales data may be required.  For the `sales_data` type, detailed sales data is expected, including item descriptions, quantities, prices, and tax rates. The data has to be passed as a valid JSON object under the `sales_data` key of the payload.  A file object is expected for the following `data_type`'s: `sales_invoice`, `purchase_invoice`, `confirmation_from_intended_receiver`, `declaration_non_receipt`, `pickup_receipt`, `recipient_id_scan`, `photo_of_parcel_exterior`, `photo_of_contents`, `photo_of_damage`, `photo_of_packaging_material_interior`, `photo_of_shipping_label`, `photo_of_parcel_weight`, `cn18_form`, `cn23_form`, `cn24_form`, `cp72_form`, `proof_of_delivery`, `proof_of_shipment`, `liability_statement`, `claim_letter`, `identity_card`. Files are expected to be passed in the `attachments` array.  Rather textual input is expected for `iban_bic`, `cellphone`, `contact_person`, `correct_address`, `description_of_contents`, `description_of_damage`, `description_of_parcel`, `email_address` data types.   The info should be passed in the `comment` field.  For the `other` type, textual input or file(s) can be expected depending on the title/description.

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
