# Toppy\Sendcloud\OrdersApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3OrdersDeleteDeleteOrder()**](OrdersApi.md#scPublicV3OrdersDeleteDeleteOrder) | **DELETE** /orders/{id} | Delete an order
[**scPublicV3OrdersGetListOrders()**](OrdersApi.md#scPublicV3OrdersGetListOrders) | **GET** /orders | Retrieve a list of orders
[**scPublicV3OrdersGetRetrieveOrder()**](OrdersApi.md#scPublicV3OrdersGetRetrieveOrder) | **GET** /orders/{id} | Retrieve an order
[**scPublicV3OrdersPatchPartialUpdateOrder()**](OrdersApi.md#scPublicV3OrdersPatchPartialUpdateOrder) | **PATCH** /orders/{id} | Update an order
[**scPublicV3OrdersPostCreateOrders()**](OrdersApi.md#scPublicV3OrdersPostCreateOrders) | **POST** /orders | Create/Update orders in batch


## `scPublicV3OrdersDeleteDeleteOrder()`

```php
scPublicV3OrdersDeleteDeleteOrder($id)
```

Delete an order

Delete an order by its unique id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud order ID

try {
    $apiInstance->scPublicV3OrdersDeleteDeleteOrder($id);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersDeleteDeleteOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud order ID |

### Return type

void (empty response body)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3OrdersGetListOrders()`

```php
scPublicV3OrdersGetListOrders($integration, $orderNumber, $orderId, $status, $orderCreatedAt, $orderCreatedAtMin, $orderCreatedAtMax, $orderUpdatedAt, $orderUpdatedAtMin, $orderUpdatedAtMax, $sort, $pageSize, $cursor): \Toppy\Sendcloud\Model\ScPublicV3OrdersGetListOrders200Response
```

Retrieve a list of orders

Get a list of orders filtered by integration, order number, order ID, order status, creation date, and update date. You can also optionally sort the results and pass a `cursor` value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$integration = 17; // int | Filter orders by one or more integration IDs. Use a comma separated list, e.g. `integration=41,68,419`.  You can get your integration IDs from the [Retrieve a list of integrations](/api/v3/integrations/retrieve-a-list-of-integrations) endpoint.
$orderNumber = ORDER_284565; // string | Filter orders by a specific order number, e.g. `order_number=ORDER_284565`. The filtering is case insensitive.
$orderId = 1896e94b-c01b-4e73-a9e7-57f51c8a4c77; // string | Filter orders by a specific order id, e.g. `order_id=1896e94b-c01b-4e73-a9e7-57f51c8a4c77`. The filtering is case insensitive.
$status = unshipped; // string | Filter orders based on their status, e.g. `status=unshipped`. The filtering is case insensitive.
$orderCreatedAt = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were created on a specific date, e.g. `order_created_at=2023-04-28`.
$orderCreatedAtMin = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were created at or after a specific date, e.g. `order_created_at_min=2023-04-28`.
$orderCreatedAtMax = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were created at or before a specific date, e.g. `order_created_at_max=2023-04-28`.
$orderUpdatedAt = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were updated on a specific date, e.g. `order_updated_at=2023-04-28`.
$orderUpdatedAtMin = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were updated at or after a specific date, e.g. `order_updated_at_min=2023-04-28`.
$orderUpdatedAtMax = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Find orders that were updated at or before a specific date, e.g. `order_updated_at_max=2023-04-28`.
$sort = -order_number; // string | Sort the orders in the response by using one or more of the following values:  - `integration`: Sort by the integration ID of the retrieved orders; to sort in descending order, use `-integration`  - `order_number`: Sort by the order number of the retrieved orders; to sort in descending order, use `-order_number`.  - `order_created_at`: Sort by the date of an order creation of the retrieved orders; to sort in descending order, use `-order_created_at`  - `order_updated_at`: Sort by the date of an order update of the retrieved orders; to sort in descending order, use `-order_updated_at`  - `pk`: Sort by the ID (autogenerated internal ID) of the retrieved orders; to sort in descending order, use `-pk`  Additional information about this query:  - Any valid combination of the above values is supported, e.g. `sort=integration,-order_created_at`.   - In case of conflicting `sort` values, e.g. `/?sort=integration,-integration`, the conflicting value will be ignored.  - If the `sort` query parameter is not set, the sorting of the retrieved orders will default to `-pk`.  - If an unsupported `sort` value is provided, the results will be sorted by the default (`-pk`).
$pageSize = 150; // float | The maximum number of results to be returned per page
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - `o`: Offset - `r`: Reverse - `p`: Position    For example, `r=1&p=300` encoded as a base64 string would be `cj0xJnA9MzAw`. The query string would then be `cursor=cj0xJnA9MzAw`.

try {
    $result = $apiInstance->scPublicV3OrdersGetListOrders($integration, $orderNumber, $orderId, $status, $orderCreatedAt, $orderCreatedAtMin, $orderCreatedAtMax, $orderUpdatedAt, $orderUpdatedAtMin, $orderUpdatedAtMax, $sort, $pageSize, $cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersGetListOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **integration** | **int**| Filter orders by one or more integration IDs. Use a comma separated list, e.g. &#x60;integration&#x3D;41,68,419&#x60;.  You can get your integration IDs from the [Retrieve a list of integrations](/api/v3/integrations/retrieve-a-list-of-integrations) endpoint. | [optional]
 **orderNumber** | **string**| Filter orders by a specific order number, e.g. &#x60;order_number&#x3D;ORDER_284565&#x60;. The filtering is case insensitive. | [optional]
 **orderId** | **string**| Filter orders by a specific order id, e.g. &#x60;order_id&#x3D;1896e94b-c01b-4e73-a9e7-57f51c8a4c77&#x60;. The filtering is case insensitive. | [optional]
 **status** | **string**| Filter orders based on their status, e.g. &#x60;status&#x3D;unshipped&#x60;. The filtering is case insensitive. | [optional]
 **orderCreatedAt** | **\DateTime**| Find orders that were created on a specific date, e.g. &#x60;order_created_at&#x3D;2023-04-28&#x60;. | [optional]
 **orderCreatedAtMin** | **\DateTime**| Find orders that were created at or after a specific date, e.g. &#x60;order_created_at_min&#x3D;2023-04-28&#x60;. | [optional]
 **orderCreatedAtMax** | **\DateTime**| Find orders that were created at or before a specific date, e.g. &#x60;order_created_at_max&#x3D;2023-04-28&#x60;. | [optional]
 **orderUpdatedAt** | **\DateTime**| Find orders that were updated on a specific date, e.g. &#x60;order_updated_at&#x3D;2023-04-28&#x60;. | [optional]
 **orderUpdatedAtMin** | **\DateTime**| Find orders that were updated at or after a specific date, e.g. &#x60;order_updated_at_min&#x3D;2023-04-28&#x60;. | [optional]
 **orderUpdatedAtMax** | **\DateTime**| Find orders that were updated at or before a specific date, e.g. &#x60;order_updated_at_max&#x3D;2023-04-28&#x60;. | [optional]
 **sort** | **string**| Sort the orders in the response by using one or more of the following values:  - &#x60;integration&#x60;: Sort by the integration ID of the retrieved orders; to sort in descending order, use &#x60;-integration&#x60;  - &#x60;order_number&#x60;: Sort by the order number of the retrieved orders; to sort in descending order, use &#x60;-order_number&#x60;.  - &#x60;order_created_at&#x60;: Sort by the date of an order creation of the retrieved orders; to sort in descending order, use &#x60;-order_created_at&#x60;  - &#x60;order_updated_at&#x60;: Sort by the date of an order update of the retrieved orders; to sort in descending order, use &#x60;-order_updated_at&#x60;  - &#x60;pk&#x60;: Sort by the ID (autogenerated internal ID) of the retrieved orders; to sort in descending order, use &#x60;-pk&#x60;  Additional information about this query:  - Any valid combination of the above values is supported, e.g. &#x60;sort&#x3D;integration,-order_created_at&#x60;.   - In case of conflicting &#x60;sort&#x60; values, e.g. &#x60;/?sort&#x3D;integration,-integration&#x60;, the conflicting value will be ignored.  - If the &#x60;sort&#x60; query parameter is not set, the sorting of the retrieved orders will default to &#x60;-pk&#x60;.  - If an unsupported &#x60;sort&#x60; value is provided, the results will be sorted by the default (&#x60;-pk&#x60;). | [optional]
 **pageSize** | **float**| The maximum number of results to be returned per page | [optional] [default to 100]
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the first page of results will be returned. To get this value, you must encode the offset, reverse and position into a base64 string.  There are 3 possible parameters to encode: - &#x60;o&#x60;: Offset - &#x60;r&#x60;: Reverse - &#x60;p&#x60;: Position    For example, &#x60;r&#x3D;1&amp;p&#x3D;300&#x60; encoded as a base64 string would be &#x60;cj0xJnA9MzAw&#x60;. The query string would then be &#x60;cursor&#x3D;cj0xJnA9MzAw&#x60;. | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersGetListOrders200Response**](../Model/ScPublicV3OrdersGetListOrders200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3OrdersGetRetrieveOrder()`

```php
scPublicV3OrdersGetRetrieveOrder($id): \Toppy\Sendcloud\Model\ScPublicV3OrdersGetRetrieveOrder200Response
```

Retrieve an order

Find a specific order by its order ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud order ID

try {
    $result = $apiInstance->scPublicV3OrdersGetRetrieveOrder($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersGetRetrieveOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud order ID |

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersGetRetrieveOrder200Response**](../Model/ScPublicV3OrdersGetRetrieveOrder200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3OrdersPatchPartialUpdateOrder()`

```php
scPublicV3OrdersPatchPartialUpdateOrder($id, $orderPartialUpdate): \Toppy\Sendcloud\Model\ScPublicV3OrdersPatchPartialUpdateOrder200Response
```

Update an order

Partially update some fields of an order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud order ID
$orderPartialUpdate = {"id":"669","order_id":"555413","order_details":{"status":{"code":"fulfilled","message":"Fulfilled"},"tags":["october_campaign"]}}; // \Toppy\Sendcloud\Model\OrderPartialUpdate | Only include the fields you would like to update. If you need to update any of the `order_items`, the `name` field is required so that the correct `order_item` is updated. If you need to add items to or remove items from an order, you should use the [Create/Update orders in batch](/api/v3/orders/create-update-orders-in-batch) endpoint instead.

try {
    $result = $apiInstance->scPublicV3OrdersPatchPartialUpdateOrder($id, $orderPartialUpdate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersPatchPartialUpdateOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud order ID |
 **orderPartialUpdate** | [**\Toppy\Sendcloud\Model\OrderPartialUpdate**](../Model/OrderPartialUpdate.md)| Only include the fields you would like to update. If you need to update any of the &#x60;order_items&#x60;, the &#x60;name&#x60; field is required so that the correct &#x60;order_item&#x60; is updated. If you need to add items to or remove items from an order, you should use the [Create/Update orders in batch](/api/v3/orders/create-update-orders-in-batch) endpoint instead. | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersPatchPartialUpdateOrder200Response**](../Model/ScPublicV3OrdersPatchPartialUpdateOrder200Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3OrdersPostCreateOrders()`

```php
scPublicV3OrdersPostCreateOrders($sendcloudPartnerId, $scPublicV3OrdersPostCreateOrdersRequestInner): \Toppy\Sendcloud\Model\ScPublicV3OrdersPostCreateOrders201Response
```

Create/Update orders in batch

Use this endpoint to insert orders into a Sendcloud API integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error.
$scPublicV3OrdersPostCreateOrdersRequestInner = [{"order_id":"555413","order_number":"OXSDFGHTD-12","order_details":{"integration":{"id":7},"status":{"code":"fulfilled","message":"Fulfilled"},"order_created_at":"2018-02-27T10:00:00.556Z","order_items":[{"name":"Cylinder candle","quantity":1,"total_price":{"value":3.5,"currency":"EUR"}}]},"payment_details":{"total_price":{"value":3.5,"currency":"EUR"},"status":{"code":"paid","message":"Paid"}},"shipping_address":{"name":"John Doe","address_line_1":"Lansdown Glade","house_number":"15","postal_code":"5341XT","city":"Oss","country_code":"NL"},"shipping_details":{"is_local_pickup":false,"delivery_indicator":"DHL home delivery","measurement":{"weight":{"value":3,"unit":"kg"}}}}]; // \Toppy\Sendcloud\Model\ScPublicV3OrdersPostCreateOrdersRequestInner[]

try {
    $result = $apiInstance->scPublicV3OrdersPostCreateOrders($sendcloudPartnerId, $scPublicV3OrdersPostCreateOrdersRequestInner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersPostCreateOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendcloudPartnerId** | **string**| If you are an official [Sendcloud Tech Partner](https://www.sendcloud.com/ecosystem/), send your unique Sendcloud Partner UUID as a request header for the system to recognize you.  The header is not required but if it is set, the system will check it. An unknown or invalid UUID will cause a 400 error. | [optional]
 **scPublicV3OrdersPostCreateOrdersRequestInner** | [**\Toppy\Sendcloud\Model\ScPublicV3OrdersPostCreateOrdersRequestInner[]**](../Model/ScPublicV3OrdersPostCreateOrdersRequestInner.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\Model\ScPublicV3OrdersPostCreateOrders201Response**](../Model/ScPublicV3OrdersPostCreateOrders201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
