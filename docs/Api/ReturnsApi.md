# Toppy\Sendcloud\ReturnsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetReturnsGetDetails()**](ReturnsApi.md#scPublicV3ScpGetReturnsGetDetails) | **GET** /returns/{id} | Retrieve a Return
[**scPublicV3ScpGetReturnsGetReturns()**](ReturnsApi.md#scPublicV3ScpGetReturnsGetReturns) | **GET** /returns | Retrieve a list of Returns
[**scPublicV3ScpPatchReturnsCancel()**](ReturnsApi.md#scPublicV3ScpPatchReturnsCancel) | **PATCH** /returns/{id}/cancel | Request cancellation of a specific Return
[**scPublicV3ScpPostReturnsCreateNewReturn()**](ReturnsApi.md#scPublicV3ScpPostReturnsCreateNewReturn) | **POST** /returns | Create a return
[**scPublicV3ScpPostReturnsCreateNewReturnSynchronously()**](ReturnsApi.md#scPublicV3ScpPostReturnsCreateNewReturnSynchronously) | **POST** /returns/announce-synchronously | Create a return synchronously
[**scPublicV3ScpPostReturnsValidate()**](ReturnsApi.md#scPublicV3ScpPostReturnsValidate) | **POST** /returns/validate | Validate a return


## `scPublicV3ScpGetReturnsGetDetails()`

```php
scPublicV3ScpGetReturnsGetDetails($id): \Toppy\Sendcloud\Model\ModelReturn
```

Retrieve a Return

Retrieve information about a specific return parcel based on the return `id`. A return `id` is assigned to every return you create in Sendcloud, and can  be retrieved for all return parcels via the `Get all returns` endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1751075; // int | The internal sendcloud id of this return (Required)

try {
    $result = $apiInstance->scPublicV3ScpGetReturnsGetDetails($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpGetReturnsGetDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The internal sendcloud id of this return (Required) |

### Return type

[**\Toppy\Sendcloud\Model\ModelReturn**](../Model/ModelReturn.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetReturnsGetReturns()`

```php
scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $cursor, $parentParcelStatus, $pageSize): \Toppy\Sendcloud\Model\ScPublicV3ScpGetReturnsGetReturns200Response
```

Retrieve a list of Returns

Retrieve a list of returns which have been created under your API credentials. The response includes return data for each parcel, plus up-to-date tracking history. The returned data is paginated and has a default number of items per page of 40 and can be controlled by the `page_size` query param. You can filter the results to only include return parcels created within a specific time frame using the `from_date` and `to_date` parameters, or based on the `parent_parcel_status`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$fromDate = 2022-04-06 00:00:00; // string | Excludes all returns before this datetime
$toDate = 2022-04-07 00:00:00; // string | Excludes all returns after this datetime
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - `o`: Offset     - `r`: Reverse     - `p`: Position   Combine into GET parameters, for example: `r=1&p=300`   Base 64 encoded it would become: `cj0xJnA9MzAw`   GET parameter in URL would be `https://some.url.com/api/endpoint/?cursor=cj0xJnA9MzAw`
$parentParcelStatus = announced; // string | Search for returns with this parent status
$pageSize = 10; // float | Refers to the number of items per page

try {
    $result = $apiInstance->scPublicV3ScpGetReturnsGetReturns($fromDate, $toDate, $cursor, $parentParcelStatus, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpGetReturnsGetReturns: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fromDate** | **string**| Excludes all returns before this datetime |
 **toDate** | **string**| Excludes all returns after this datetime |
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - &#x60;o&#x60;: Offset     - &#x60;r&#x60;: Reverse     - &#x60;p&#x60;: Position   Combine into GET parameters, for example: &#x60;r&#x3D;1&amp;p&#x3D;300&#x60;   Base 64 encoded it would become: &#x60;cj0xJnA9MzAw&#x60;   GET parameter in URL would be &#x60;https://some.url.com/api/endpoint/?cursor&#x3D;cj0xJnA9MzAw&#x60; | [optional]
 **parentParcelStatus** | **string**| Search for returns with this parent status | [optional]
 **pageSize** | **float**| Refers to the number of items per page | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetReturnsGetReturns200Response**](../Model/ScPublicV3ScpGetReturnsGetReturns200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPatchReturnsCancel()`

```php
scPublicV3ScpPatchReturnsCancel($id): \Toppy\Sendcloud\Model\ScPublicV3ScpPatchReturnsCancel202Response
```

Request cancellation of a specific Return

You can request cancellation for a return by providing the return `id` to this endpoint. Not all carriers support upstream label cancellation via an API request, therefore this endpoint will only send a cancellation **request**. A successful response indicates that the request is received and the carrier supports label cancellation.  You can check the `parent_status` of the return via the `Get a specific return` endpoint to confirm whether the actual cancellation was successful.  <!-- theme: info --> >You can find more information about carriers which do not support label cancellation requests on our <a href=\"https://support.sendcloud.com/hc/en-us/articles/4461608475284-How-to-cancel-a-return-shipment\">**Help Center**</a>.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 1751075; // int | The internal sendcloud id of this return (Required)

try {
    $result = $apiInstance->scPublicV3ScpPatchReturnsCancel($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPatchReturnsCancel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The internal sendcloud id of this return (Required) |

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPatchReturnsCancel202Response**](../Model/ScPublicV3ScpPatchReturnsCancel202Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsCreateNewReturn()`

```php
scPublicV3ScpPostReturnsCreateNewReturn($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return

The `Create a return` endpoint is the heart of the Return API; it allows you to create a stand-alone return, based mainly on the `to` and `from_address`, parcel `weight` and the `ship_with` object.  You can provide a list of items and item descriptions to be included in the return via the `parcel_items` field (optional).  <!-- theme: info --> >The `parcel_items` field is **mandatory** if you're creating a return from outside-EU. This is because information about the parcel contents must be provided in order to generate the required customs documents.  ### The ship_with object  This object is used to select a shipping method for the return. There are two ways of selecting a shipping method: - By providing a `shipping_option_code` (find the code using [shipping options API](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipping-options/operations/create-a-fetch-shipping-option)). - By providing a `shipping_product_code` and a set of `functionalities`.    Functionalities are used to filter the right shipping method within the product. Find all these data using [shipping products API](https://api.sendcloud.dev/docs/sendcloud-public-api/shipping-products/operations/list-shipping-products)).  The `contract` attribute refers to the ID of a direct contract you have with the carrier. Get the IDs for your contracts from [**Retrieve a list of contracts**](https://api.sendcloud.dev/docs/sendcloud-public-api/contracts/operations/list-contracts).  <!-- theme: warning --> > If you have more than one active contract for a specific carrier, you must fill the `contract` attribute with your desired contract ID in your request.  ### Retrieve return shipping products  In your request, you must provide an appropriate `shipping_product_code` and a set of `functionalities` inside the `ship_with` object. To find a suitable product, refer to the following endpoint: <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/shipping-products/operations/list-shipping-products\">**Retrieve a list of shipping products**</a>.  You can filter for a return method by flagging the `returns` field as `true`,  and by including the `from_country` and `to_country` fields. The more fields you specify, the more refined the results will be. This helps you find the most appropriate shipping product for your return parcel.  It's also possible to filter based on your preferred <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/shipping-products/operations/list-shipping-functionalities\">**shipping functionality**</a>, e.g. `age_check=18`, `delivery_before`, etc.  ### Add return reasons You can (optionally) assign a **return reason** to `parcel_items` by providing a`return_reason_id` and entering a value from the key below. Assigning return reasons to items provides you with analyzable data you can use to predict return trends or identify issues with particular products.  | Return Reason ID | Description                                  | | ---------------- | -------------------------------------------- | | 1                | Product did not match expectations           | | 3                | Other (explain in message)                   | | 4                | Incorrect product ordered                    | | 6                | Product did not match description on website | | 7                | Wrong product shipped                        | | 8                | No reason                                    | | 9                | Rent                                         | | 10               | Does not work                                | | 11               | Changed my mind                              | | 12               | Did not meet expectations                    | | 13               | Excessive amount                             | | 14               | Better price available                       | | 15               | Accidental order                             | | 16               | No longer needed                             | | 17               | Sample products                              | | 18               | Looks different than expected                | | 19               | Ordered more than one size                   | | 20               | Arrived too late                             | | 21               | Poor quality / Faulty                        | | 22               | Does not fit properly                        | | 23               | Does not suit me                             | | 24               | Incorrect product received                   | | 25               | Parcel damaged on arrival                    | | 26               | Wrong size ordered                           | | 27               | Wrong color ordered                          | | 28               | Does not function as expected                | | 29               | Recycle or reuse packaging                   | | 30               | Size too large                               | | 31               | Size too small                               | | 32               | Holiday season return                        |  ### Retrieve the shipping label for this return  Once the parcel for the created return is announced, you can download the shipping label for it.  Find the documentation on how to retrieve a label for a parcel on the <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/labels/operations/get-a-label-normal-printer\">**Retrieve a PDF label**</a> endpoint.  The url for downloading the label is also available on the Return object (Only if the parcel is announced). To retrieve a Return, take a look at <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/returns/operations/get-a-return\">**Retrieve a Return**</a>.  To learn more about all the options for retrieving labels and customs declaration documents, refer to the <a href=\"https://api.sendcloud.dev/docs/sendcloud-public-api/labels\">**Labels**</a> section of the API V2 documentation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturn($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturn: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsCreateNewReturnSynchronously()`

```php
scPublicV3ScpPostReturnsCreateNewReturnSynchronously($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response
```

Create a return synchronously

This endpoint will create a return, similarly to the [Create a return](https://api.sendcloud.dev/docs/sendcloud-public-api/returns/operations/create-a-return) endpoint, but via a synchronous API request. This means that the API will wait for a response from the carrier before you can continue.  This endpoint is primarily used for **debugging purposes** in the event that a return parcel announcement fails, as it will retrieve the carrier announcement error. Creating a return synchronously can impact the performance of the endpoint, as the process will take longer than calls to the `Create a return` endpoint.  **Note:** The `parcel_items` field is mandatory if you're creating a return from outside-EU.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsCreateNewReturnSynchronously($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsCreateNewReturnSynchronously: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturn201Response**](../Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostReturnsValidate()`

```php
scPublicV3ScpPostReturnsValidate($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest): \Toppy\Sendcloud\Model\ReturnValidation
```

Validate a return

This endpoint allows you to validate whether a return can be announced **without** actually creating the return or announcing it with the carrier. You can structure the request body exactly as you would if you were making a request to the `Create a return` endpoint.  When you make the request, the response will indicate whether the parcel is valid and can be announced. Validation is based mainly on the `to` and `from` address, the parcel `weight` and the shipping product `id` provided.  **Note:** The `parcel_items` field is mandatory if you're creating a return from outside-EU.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ReturnsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3ScpPostReturnsCreateNewReturnRequest = {"from_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"to_address":{"name":"My name","company_name":"Sendcloud","address_line_1":"Stadhuisplein","house_number":"50","postal_code":"1013 AB","city":"Amsterdam","country_code":"NL","phone_number":"+319881729999","email":"test@test.com"},"ship_with":{"type":"shipping_option_code","shipping_option_code":"dpd:return/return","contract":123456},"dimensions":{"height":10,"width":10,"length":10,"unit":"cm"},"weight":{"value":0.4,"unit":"kg"},"collo_count":1,"parcel_items":[{"description":"T-Shirt XL","quantity":1,"weight":{"value":0.4,"unit":"kg"},"value":{"value":6.15,"currency":"EUR"},"hs_code":"6205.20","origin_country":"NL","sku":"TS1234","product_id":"19283"}],"send_tracking_emails":false,"brand_id":1,"total_insured_value":{"value":6.15,"currency":"EUR"},"order_number":"ORD123456","total_order_value":{"value":6.15,"currency":"EUR"},"external_reference":"RET98765","customs_invoice_nr":"test_invoice_123","delivery_option":"drop_off_point"}; // \Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest

try {
    $result = $apiInstance->scPublicV3ScpPostReturnsValidate($sendcloudPartnerId, $scPublicV3ScpPostReturnsCreateNewReturnRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnsApi->scPublicV3ScpPostReturnsValidate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;,  you can provide this additional request header for the system to recognize you.  Sendcloud Partner UUID is provided to Sendcloud partners. The header is not required but if it is set,  the system will validate it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3ScpPostReturnsCreateNewReturnRequest** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpPostReturnsCreateNewReturnRequest**](../Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ReturnValidation**](../Model/ReturnValidation.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
