# Toppy\Sendcloud\ShipmentsApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3ScpGetAllShipments()**](ShipmentsApi.md#scPublicV3ScpGetAllShipments) | **GET** /shipments | Retrieve shipments
[**scPublicV3ScpGetShipmentById()**](ShipmentsApi.md#scPublicV3ScpGetShipmentById) | **GET** /shipments/{id} | Retrieve a shipment
[**scPublicV3ScpPostAnnounceShipment()**](ShipmentsApi.md#scPublicV3ScpPostAnnounceShipment) | **POST** /shipments/announce | Create and announce a shipment synchronously
[**scPublicV3ScpPostAnnounceShipmentWithRules()**](ShipmentsApi.md#scPublicV3ScpPostAnnounceShipmentWithRules) | **POST** /shipments/announce-with-shipping-rules | Create a shipment with rules and / or defaults and announce it synchronously
[**scPublicV3ScpPostCancelShipment()**](ShipmentsApi.md#scPublicV3ScpPostCancelShipment) | **POST** /shipments/{id}/cancel | Cancel a shipment
[**scPublicV3ScpPostCreateShipment()**](ShipmentsApi.md#scPublicV3ScpPostCreateShipment) | **POST** /shipments | Create and announce a shipment asynchronously
[**scPublicV3ScpPostCreateShipmentWithRules()**](ShipmentsApi.md#scPublicV3ScpPostCreateShipmentWithRules) | **POST** /shipments/create-with-shipping-rules | Create a shipment with rules and / or defaults and announce it asynchronously


## `scPublicV3ScpGetAllShipments()`

```php
scPublicV3ScpGetAllShipments($parcelStatus, $trackingNumber, $externalReferenceId, $orderNumber, $integrationId, $updatedBefore, $updatedAfter, $announcedBefore, $announcedAfter, $ids, $cursor, $pageSize): \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllShipments200Response
```

Retrieve shipments

This endpoint allows you to retrieve a list of all the shipments which you have created or imported into your Sendcloud account under your API credentials. You can filter the results based on the query parameters provided below, in order to retrieve a specific shipment or list of shipments which match the defined criteria.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$parcelStatus = new \Toppy\Sendcloud\Model\\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter(); // \Toppy\Sendcloud\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter | Returns shipments that have the requested status. For a list of possible statuses, see the [Parcel statuses](https://api.sendcloud.dev/docs/sendcloud-public-api/parcel-statuses/operations/list-parcel-statuses) endpoint
$trackingNumber = 'trackingNumber_example'; // string | Returns shipments that match a specified tracking number
$externalReferenceId = 'externalReferenceId_example'; // string | Returns shipments that match a specified external reference
$orderNumber = 'orderNumber_example'; // string | Returns a shipment that matches a specific `order_number` property from your shipments
$integrationId = 'integrationId_example'; // string | Returns all shipments that matches a specific `integration_id` property from your shipments
$updatedBefore = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been updated in our system before a given time. You can use the value of ISO 8601 DateTime string like this
$updatedAfter = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been updated in our system after a given time. You can use the value of ISO 8601 DateTime string like this
$announcedBefore = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been announced to the carrier before the given time. You can use the value of ISO 8601 DateTime string like this
$announcedAfter = 2018-02-26T11:01:47.505309+00:00; // string | Returns all shipments which have been announced to the carrier after the given time. You can use the value of ISO 8601 DateTime string like this
$ids = 13579,24680,12345; // string | Filter results using a list of shipments IDs. This is a comma separated list of IDs, it may not contain more then 100 IDs.
$cursor = cj0xJnA9MzAw; // string | The cursor query string will be used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters. example:   For a cursor string there are 3 possible parameters to encode:    - o: Offset    - r: Reverse    - p: Position   Combine into GET parameters. Example: r=1&p=300   Base 64 encoded it would become: cj0xJnA9MzAw   GET parameter in url would be https://some.url.com/api/endpoint/?cursor=cj0xJnA9MzAw
$pageSize = 10; // int | The maximum number of items to be returned in the response.

try {
    $result = $apiInstance->scPublicV3ScpGetAllShipments($parcelStatus, $trackingNumber, $externalReferenceId, $orderNumber, $integrationId, $updatedBefore, $updatedAfter, $announcedBefore, $announcedAfter, $ids, $cursor, $pageSize);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpGetAllShipments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **parcelStatus** | [**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllShipmentsParcelStatusParameter**](../Model/.md)| Returns shipments that have the requested status. For a list of possible statuses, see the [Parcel statuses](https://api.sendcloud.dev/docs/sendcloud-public-api/parcel-statuses/operations/list-parcel-statuses) endpoint | [optional]
 **trackingNumber** | **string**| Returns shipments that match a specified tracking number | [optional]
 **externalReferenceId** | **string**| Returns shipments that match a specified external reference | [optional]
 **orderNumber** | **string**| Returns a shipment that matches a specific &#x60;order_number&#x60; property from your shipments | [optional]
 **integrationId** | **string**| Returns all shipments that matches a specific &#x60;integration_id&#x60; property from your shipments | [optional]
 **updatedBefore** | **string**| Returns all shipments which have been updated in our system before a given time. You can use the value of ISO 8601 DateTime string like this | [optional]
 **updatedAfter** | **string**| Returns all shipments which have been updated in our system after a given time. You can use the value of ISO 8601 DateTime string like this | [optional]
 **announcedBefore** | **string**| Returns all shipments which have been announced to the carrier before the given time. You can use the value of ISO 8601 DateTime string like this | [optional]
 **announcedAfter** | **string**| Returns all shipments which have been announced to the carrier after the given time. You can use the value of ISO 8601 DateTime string like this | [optional]
 **ids** | **string**| Filter results using a list of shipments IDs. This is a comma separated list of IDs, it may not contain more then 100 IDs. | [optional]
 **cursor** | **string**| The cursor query string will be used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters. example:   For a cursor string there are 3 possible parameters to encode:    - o: Offset    - r: Reverse    - p: Position   Combine into GET parameters. Example: r&#x3D;1&amp;p&#x3D;300   Base 64 encoded it would become: cj0xJnA9MzAw   GET parameter in url would be https://some.url.com/api/endpoint/?cursor&#x3D;cj0xJnA9MzAw | [optional]
 **pageSize** | **int**| The maximum number of items to be returned in the response. | [optional] [default to 40]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetAllShipments200Response**](../Model/ScPublicV3ScpGetAllShipments200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpGetShipmentById()`

```php
scPublicV3ScpGetShipmentById($id): \Toppy\Sendcloud\Model\ScPublicV3ScpGetShipmentById200Response
```

Retrieve a shipment

This endpoint allows you to retrieve a specific shipment created under your Sendcloud credentials, based on the shipment `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the shipment you want to retrieve

try {
    $result = $apiInstance->scPublicV3ScpGetShipmentById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpGetShipmentById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| The id of the shipment you want to retrieve |

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3ScpGetShipmentById200Response**](../Model/ScPublicV3ScpGetShipmentById200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostAnnounceShipment()`

```php
scPublicV3ScpPostAnnounceShipment($sendcloudPartnerId, $shipmentRequestSyncAnnounce): \Toppy\Sendcloud\Model\AnnouncedShipmentIncludingLabel
```

Create and announce a shipment synchronously

This endpoint **announces a shipment synchronously** under your API credentials.  ### International shipments  If you want to create a shipment to be sent to a destination country outside the EU, it's mandatory to include additional information related to the shipment contents. This allows Sendcloud to automatically generate the required customs documentation based on the international shipping option selected. After the shipping label and associated documents are generated, you can retrieve and download them via the [**Retrieve a parcel document**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/parcel-documents/operations/get-retrieve-parcel-documents) endpoint. Note that when passing along prices, mixed currencies are not accepted. Therefore, ensure that all price fields use the same currency.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400.
$shipmentRequestSyncAnnounce = {"label_details":{"mime_type":"application/pdf","dpi":72},"to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"label_notes":["I live at the blue door","The doorbell isn’t working"],"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\Model\ShipmentRequestSyncAnnounce | 

try {
    $result = $apiInstance->scPublicV3ScpPostAnnounceShipment($sendcloudPartnerId, $shipmentRequestSyncAnnounce);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostAnnounceShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400. | [optional]
 **shipmentRequestSyncAnnounce** | [**\Toppy\Sendcloud\Model\ShipmentRequestSyncAnnounce**](../Model/ShipmentRequestSyncAnnounce.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\AnnouncedShipmentIncludingLabel**](../Model/AnnouncedShipmentIncludingLabel.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostAnnounceShipmentWithRules()`

```php
scPublicV3ScpPostAnnounceShipmentWithRules($sendcloudPartnerId, $shipmentRequestWithRules): \Toppy\Sendcloud\Model\AnnouncedShipmentIncludingLabel
```

Create a shipment with rules and / or defaults and announce it synchronously

The main advantage of this endpoint over the [Create and announce a shipment](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipments/operations/create-a-shipment-announce) endpoint (and also the difference between those) is the ability to apply shipping [rules](https://app.sendcloud.com/v2/shipping/rules) and [defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults) to a shipment, and due to that, more fields become optional compared to that Shipments V3 sync endpoint.  **Note: the shipment (parcels) will be linked to the integration identified through the API credentials from the request authentication (`Basic ...`).**  ### Development status This endpoint is currently in <a href=\"https://support.sendcloud.com/hc/en-us/articles/4417167140756-What-is-beta-\">**beta**</a>, meaning that it is still under development. During this phase, we continually monitor and test the API to improve its performance, review the requested and the returned data, and uncover any potential bugs that could have a future impact on our users.  <!-- theme: warning --> >**Please note that there is a possibility of experiencing breaking changes while it is still in beta**.  ### Shipping rules  **Notes**: - **Due to the data (shipments) that we receive in this API, NOT all of the shipping rules (actions or conditions) can (and will) be applied.** - **Shipping rules do not fully apply to multicollo shipments.   In such cases, the rule conditions for weight, parcel dimensions (height, length, width), total order value, item name, item quantity, item SKU and total parcel item value will not be matched.   Additionally, the following actions will not be triggered:**   - Using a box (Use box)   - Setting the weight (Set weight)   - Setting the number of parcels (Set number of parcels)   - Insuring the shipment value (Insure shipment value by)   - Insuring it by percentage (Insure shipment value by %)   - Increasing item value by percentage (Decrease item value by %)   - Setting item HS code (Set Item HS Code)   - Setting item name (Set item name)   - Setting item origin country (Set Item Origin Country)   - Setting item value (Set item value)   - Setting item weight (Set item weight) **Please consider this limitation when defining rules.**  **Here's a list of the shipping rules conditions (if) that can be applied:** - Carrier - Checkout delivery method - Company name - Customer email - Integration - Item SKU - Item name - Item quantity - Parcel height (cm) - Parcel length (cm) - Parcel width (cm) - Phone number - Postal code - To country - Total order value - Total parcel item value - Weight (kg)  **Here's a list of the shipping rules actions (then) that can be applied:** - Add customs declaration statement - Use box - Decrease item value by % - Insure shipment value by - Insure shipment value by % - Set customs general notes - Set customer email - Set Item HS Code - Set item name - Set Item Origin Country - Set item value - Set item weight - Set number of parcels - Phone number - Ship with address - Ship with - Set weight - Use shipping contract

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400.
$shipmentRequestWithRules = {"apply_shipping_defaults":true,"apply_shipping_rules":true,"delivery_indicator":"DHL home delivery","to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\Model\ShipmentRequestWithRules | 

try {
    $result = $apiInstance->scPublicV3ScpPostAnnounceShipmentWithRules($sendcloudPartnerId, $shipmentRequestWithRules);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostAnnounceShipmentWithRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400. | [optional]
 **shipmentRequestWithRules** | [**\Toppy\Sendcloud\Model\ShipmentRequestWithRules**](../Model/ShipmentRequestWithRules.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\AnnouncedShipmentIncludingLabel**](../Model/AnnouncedShipmentIncludingLabel.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCancelShipment()`

```php
scPublicV3ScpPostCancelShipment($id): \Toppy\Sendcloud\Model\CancelShipmentStatus
```

Cancel a shipment

You can use this endpoint to **Cancel** an announced shipment.  ### Cancelling a shipment When you **cancel** a shipment which is already announced (has shipping labels attached to it), you will still be able to find it via the `id` and the [**Retrieve a shipment**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipments/operations/get-shipment-by-id) endpoint. In the Sendcloud panel, it will appear in your **Cancelled labels** overview.  **Insurance Notice**: If you proceed to send a shipment that was initially cancelled, the parcel's insurance coverage will become void, and any insurance claims will not be valid for that shipment.  <!-- theme: warning --> >After 42 days, it's no longer possible to cancel a shipment, even if it hasn't been sent.  ### Conditions for label cancellation  It's not always possible to cancel a shipment whose parcel has already been announced. As a result, cancellation is not guaranteed and may be asynchronous depending on the state of the shipment parcel. When you send a cancellation request via this endpoint, the response will indicate the status of the cancellation request.  <!-- theme: info --> >Each carrier will have different cancellation deadlines. Some carriers do not accept cancellation requests regardless of whether or not the label is cancelled within the deadline. You can find more information about cancellation deadlines on our <a href=\"https://support.sendcloud.com/hc/en-us/articles/360025143991-How-do-I-cancel-my-shipment-\">**Help Center**.</a>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID of the shipment

try {
    $result = $apiInstance->scPublicV3ScpPostCancelShipment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCancelShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| ID of the shipment |

### Return type

[**\Toppy\Sendcloud\Model\CancelShipmentStatus**](../Model/CancelShipmentStatus.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCreateShipment()`

```php
scPublicV3ScpPostCreateShipment($sendcloudPartnerId, $shipmentRequestAsync): \Toppy\Sendcloud\Model\ShipmentCreatedResponse
```

Create and announce a shipment asynchronously

This endpoint **announces a shipment asynchronously** under your API credentials.  ### International shipments  If you want to create a shipment to be sent to a destination country outside the EU, it's mandatory to include additional information related to the shipment contents. This allows Sendcloud to automatically generate the required customs documentation based on the international shipping option selected. After the shipping label and associated documents are generated, you can retrieve and download them via the [**Retrieve a parcel document**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/parcel-documents/operations/get-retrieve-parcel-documents) endpoint. Note that when passing along prices, mixed currencies are not accepted. Therefore, ensure that all price fields use the same currency.  ### Multicollo  More information on how to create multiple parcels within one shipment can be found on the [related page](https://sendcloud.dev/docs/shipping/multicollo/) of our developers portal.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400.
$shipmentRequestAsync = {"to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\Model\ShipmentRequestAsync | 

try {
    $result = $apiInstance->scPublicV3ScpPostCreateShipment($sendcloudPartnerId, $shipmentRequestAsync);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCreateShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400. | [optional]
 **shipmentRequestAsync** | [**\Toppy\Sendcloud\Model\ShipmentRequestAsync**](../Model/ShipmentRequestAsync.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ShipmentCreatedResponse**](../Model/ShipmentCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3ScpPostCreateShipmentWithRules()`

```php
scPublicV3ScpPostCreateShipmentWithRules($sendcloudPartnerId, $shipmentRequestWithRules): \Toppy\Sendcloud\Model\ShipmentCreatedResponse
```

Create a shipment with rules and / or defaults and announce it asynchronously

The main advantage of this endpoint over the [Create and announce a shipment asynchronously](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipments/operations/create-a-shipment) endpoint (and also the difference between those) is the ability to apply shipping [rules](https://app.sendcloud.com/v2/shipping/rules) and [defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults) to a shipment, and due to that, more fields become optional compared to that Shipments V3 async endpoint.  **Note: the shipment (parcels) will be linked to the integration identified through the API credentials from the request authentication (`Basic ...`).**  ### Development status This endpoint is currently in <a href=\"https://support.sendcloud.com/hc/en-us/articles/4417167140756-What-is-beta-\">**beta**</a>, meaning that it is still under development. During this phase, we continually monitor and test the API to improve its performance, review the requested and the returned data, and uncover any potential bugs that could have a future impact on our users.  <!-- theme: warning --> >**Please note that there is a possibility of experiencing breaking changes while it is still in beta**.  ### Shipping rules  **Notes**: - **Due to the data (shipments) that we receive in this API, NOT all of the shipping rules (actions or conditions) can (and will) be applied.** - **Shipping rules do not fully apply to multicollo shipments.   In such cases, the rule conditions for weight, parcel dimensions (height, length, width), total order value, item name, item quantity, item SKU and total parcel item value will not be matched.   Additionally, the following actions will not be triggered:**   - Using a box (Use box)   - Setting the weight (Set weight)   - Setting the number of parcels (Set number of parcels)   - Insuring the shipment value (Insure shipment value by)   - Insuring it by percentage (Insure shipment value by %)   - Increasing item value by percentage (Decrease item value by %)   - Setting item HS code (Set Item HS Code)   - Setting item name (Set item name)   - Setting item origin country (Set Item Origin Country)   - Setting item value (Set item value)   - Setting item weight (Set item weight) **Please consider this limitation when defining rules.**  **Here's a list of the shipping rules conditions (if) that can be applied:** - Carrier - Checkout delivery method - Company name - Customer email - Integration - Item SKU - Item name - Item quantity - Parcel height (cm) - Parcel length (cm) - Parcel width (cm) - Phone number - Postal code - To country - Total order value - Total parcel item value - Weight (kg)  **Here's a list of the shipping rules actions (then) that can be applied:** - Add customs declaration statement - Use box - Decrease item value by % - Insure shipment value by - Insure shipment value by % - Set customs general notes - Set customer email - Set Item HS Code - Set item name - Set Item Origin Country - Set item value - Set item weight - Set number of parcels - Phone number - Ship with address - Ship with - Set weight - Use shipping contract

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 550e8400-e29b-41d4-a716-446655440000; // string | If you are <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\"> an official Sendcloud Tech Partner</a>, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400.
$shipmentRequestWithRules = {"apply_shipping_defaults":true,"apply_shipping_rules":true,"delivery_indicator":"DHL home delivery","to_address":{"name":"John Doe","company_name":"Sendcloud","address_line_1":"Insulindelaan 115","house_number":"115","postal_code":"5642CV","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"john.doe@sendcloud.com","po_box":"PO Box 678"},"from_address":{"name":"Marie Doe","company_name":"Sendcloud","address_line_1":"Stadhuisplein 10","address_line_2":"2e verdieping","house_number":"10","postal_code":"5611 EM","city":"Eindhoven","country_code":"NL","phone_number":"+31612345678","email":"marie.doe@sendcloud.com","po_box":"PO Box 478"},"ship_with":{"type":"shipping_option_code","properties":{"shipping_option_code":"postnl:standard","contract_id":517}},"order_number":"1234567890","total_order_price":{"currency":"EUR","value":"11.11"},"parcels":[{"dimensions":{"length":"5.00","width":"15.00","height":"20.00","unit":"cm"},"weight":{"value":"1.320","unit":"kg"},"parcel_items":[{"item_id":"5552","description":"T-Shirt XL","quantity":1,"weight":{"value":0.3,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"NL","sku":"TS1234","product_id":"19284","mid_code":"NLOZR92MEL","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":"XL","color":"green"}},{"item_id":"98712","description":"Sneakers 42","quantity":1,"weight":{"value":1.02,"unit":"kg"},"price":{"value":12.65,"currency":"EUR"},"hs_code":"620520","origin_country":"US","sku":"TS1234","product_id":"19284","mid_code":"US1234567","material_content":"100% Cotton","intended_use":"Personal use","dds_reference":"25FIYPEK0A7573","taric_doc_code":"Y142","properties":{"size":42,"color":"black"}}]}]}; // \Toppy\Sendcloud\Model\ShipmentRequestWithRules | 

try {
    $result = $apiInstance->scPublicV3ScpPostCreateShipmentWithRules($sendcloudPartnerId, $shipmentRequestWithRules);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->scPublicV3ScpPostCreateShipmentWithRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt; an official Sendcloud Tech Partner&lt;/a&gt;, you can provide this additional request header for the system to recognize you. Sendcloud Partner UUID is provided to Sendcloud partners. The token is not required but if the header is set, the system will try to validate it. An unknown UUID will cause the 404 return, whilst an invalid one will return 400. | [optional]
 **shipmentRequestWithRules** | [**\Toppy\Sendcloud\Model\ShipmentRequestWithRules**](../Model/ShipmentRequestWithRules.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ShipmentCreatedResponse**](../Model/ShipmentCreatedResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
