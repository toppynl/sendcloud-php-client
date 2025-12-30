# Toppy\Sendcloud\OrdersApi

All URIs are relative to https://account.sendcloud.com.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3OrdersDeleteDeleteOrder()**](OrdersApi.md#scPublicV3OrdersDeleteDeleteOrder) | **DELETE** /orders/{id} | Delete an order
[**scPublicV3OrdersGetListOrders()**](OrdersApi.md#scPublicV3OrdersGetListOrders) | **GET** /orders | Retrieve orders from integrations
[**scPublicV3OrdersGetRetrieveOrder()**](OrdersApi.md#scPublicV3OrdersGetRetrieveOrder) | **GET** /orders/{id} | Retrieving a specific order
[**scPublicV3OrdersPatchPartialUpdateOrder()**](OrdersApi.md#scPublicV3OrdersPatchPartialUpdateOrder) | **PATCH** /orders/{id} | Update an order
[**scPublicV3OrdersPostCreateOrders()**](OrdersApi.md#scPublicV3OrdersPostCreateOrders) | **POST** /orders | Create/Update orders in batch


## `scPublicV3OrdersDeleteDeleteOrder()`

```php
scPublicV3OrdersDeleteDeleteOrder($id)
```

Delete an order

This method allows to delete an order in particular.

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

Retrieve orders from integrations

You can get the list of orders via the API the same way you can find it on the Incoming Orders panel. The endpoint is paginated, you can navigate through the results by using the URLs of the `next` and `prev` fields in the Link response header.

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
$integration = 17; // int | Filter orders by integration ID or IDs. Use comma separated list, for example \"/?integration=41,68,419\". To obtain the integration IDs, you can utilize the integration [endpoint](https://api.sendcloud.dev/docs/sendcloud-public-api/integrations/operations/list-integrations) listings.
$orderNumber = ORDER_284565; // string | Filter orders by a specific order number. For example \"/?order_number=ORDER_284565\". The filter handles capital letters the same as lowercase letters. The field used is `order_number` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderId = 1896e94b-c01b-4e73-a9e7-57f51c8a4c77; // string | Filter orders by a specific order id. For example \"/?order_id=1896e94b-c01b-4e73-a9e7-57f51c8a4c77\". The filter handles capital letters the same as lowercase letters. The field used is `order_id` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$status = unshipped; // string | Filter orders based on their status. For example \"/?status=unshipped\". The filter handles capital letters the same as lowercase letters. The field used is `order_details` -> `status` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderCreatedAt = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders based on a specific date. For example \"/?order_created_at=2023-04-28\". The field used is `order_details` -> `order_created_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderCreatedAtMin = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders that are created at or after a specific date. For example \"/?order_created_at_min=2023-04-28\". The field used is `order_details` -> `order_created_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderCreatedAtMax = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders that are created at or before a specific date. For example \"/?order_created_at_max=2023-04-28\". The field used is `order_details` -> `order_created_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderUpdatedAt = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders based on a specific date. For example \"/?order_updated_at=2023-04-28\". The field used is `order_details` -> `order_updated_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderUpdatedAtMin = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders that are created at or after a specific date. For example \"/?order_updated_at_min=2023-04-28\". The field used is `order_details` -> `order_updated_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$orderUpdatedAtMax = Fri Apr 28 02:00:00 CEST 2023; // \DateTime | Filter orders that are created at or before a specific date. For example \"/?order_updated_at_max=2023-04-28\". The field used is `order_details` -> `order_updated_at` within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order)
$sort = -order_number; // string | Sort the retrieved orders on attributes of the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) by setting the sort query. The attributes below can be used to sort the orders in the response:  - `integration`: Sort by the integration ID of the retrieved orders; to sort in descending order, use `-integration`  - `order_number`: Sort by the order number of the retrieved orders; to sort in descending order, use `-order_number`.  - `order_created_at`: Sort by the date of an order creation of the retrieved orders; to sort in descending order, use `-order_created_at`  - `order_updated_at`: Sort by the date of an order update of the retrieved orders; to sort in descending order, use `-order_updated_at`  - `pk`: Sort by the ID (autogenerated internal ID) of the retrieved orders; to sort in descending order, use `-pk` Additional information about this query:  - Any valid combination of all these supported values is supported, eg., `/?sort=\"integration,-order_created_at\"`.   - In case of conflicting `sort` values eg., `/?sort=\"integration,-integration\"`, the conflicting value will be ignored.  - If the `sort` query parameter is not set, the sorting of the retrieved orders will be defaulted to `-pk`.  - In case where an unsupported `sort` value is provided, the results will be sorted by the default (`-pk`).
$pageSize = 150; // float | The maximum number of results to be returned per page
$cursor = cj0xJnA9MzAw; // string | The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - `o`: Offset     - `r`: Reverse     - `p`: Position   Combine into GET parameters, for example: `r=1&p=300`   Base 64 encoded it would become: `cj0xJnA9MzAw`   GET parameter in URL would be `https://some.url.com/api/endpoint/?cursor=cj0xJnA9MzAw`

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
 **integration** | **int**| Filter orders by integration ID or IDs. Use comma separated list, for example \&quot;/?integration&#x3D;41,68,419\&quot;. To obtain the integration IDs, you can utilize the integration [endpoint](https://api.sendcloud.dev/docs/sendcloud-public-api/integrations/operations/list-integrations) listings. | [optional]
 **orderNumber** | **string**| Filter orders by a specific order number. For example \&quot;/?order_number&#x3D;ORDER_284565\&quot;. The filter handles capital letters the same as lowercase letters. The field used is &#x60;order_number&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderId** | **string**| Filter orders by a specific order id. For example \&quot;/?order_id&#x3D;1896e94b-c01b-4e73-a9e7-57f51c8a4c77\&quot;. The filter handles capital letters the same as lowercase letters. The field used is &#x60;order_id&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **status** | **string**| Filter orders based on their status. For example \&quot;/?status&#x3D;unshipped\&quot;. The filter handles capital letters the same as lowercase letters. The field used is &#x60;order_details&#x60; -&gt; &#x60;status&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderCreatedAt** | **\DateTime**| Filter orders based on a specific date. For example \&quot;/?order_created_at&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_created_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderCreatedAtMin** | **\DateTime**| Filter orders that are created at or after a specific date. For example \&quot;/?order_created_at_min&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_created_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderCreatedAtMax** | **\DateTime**| Filter orders that are created at or before a specific date. For example \&quot;/?order_created_at_max&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_created_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderUpdatedAt** | **\DateTime**| Filter orders based on a specific date. For example \&quot;/?order_updated_at&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_updated_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderUpdatedAtMin** | **\DateTime**| Filter orders that are created at or after a specific date. For example \&quot;/?order_updated_at_min&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_updated_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **orderUpdatedAtMax** | **\DateTime**| Filter orders that are created at or before a specific date. For example \&quot;/?order_updated_at_max&#x3D;2023-04-28\&quot;. The field used is &#x60;order_details&#x60; -&gt; &#x60;order_updated_at&#x60; within the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) | [optional]
 **sort** | **string**| Sort the retrieved orders on attributes of the [Order model](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/orders/schemas/order) by setting the sort query. The attributes below can be used to sort the orders in the response:  - &#x60;integration&#x60;: Sort by the integration ID of the retrieved orders; to sort in descending order, use &#x60;-integration&#x60;  - &#x60;order_number&#x60;: Sort by the order number of the retrieved orders; to sort in descending order, use &#x60;-order_number&#x60;.  - &#x60;order_created_at&#x60;: Sort by the date of an order creation of the retrieved orders; to sort in descending order, use &#x60;-order_created_at&#x60;  - &#x60;order_updated_at&#x60;: Sort by the date of an order update of the retrieved orders; to sort in descending order, use &#x60;-order_updated_at&#x60;  - &#x60;pk&#x60;: Sort by the ID (autogenerated internal ID) of the retrieved orders; to sort in descending order, use &#x60;-pk&#x60; Additional information about this query:  - Any valid combination of all these supported values is supported, eg., &#x60;/?sort&#x3D;\&quot;integration,-order_created_at\&quot;&#x60;.   - In case of conflicting &#x60;sort&#x60; values eg., &#x60;/?sort&#x3D;\&quot;integration,-integration\&quot;&#x60;, the conflicting value will be ignored.  - If the &#x60;sort&#x60; query parameter is not set, the sorting of the retrieved orders will be defaulted to &#x60;-pk&#x60;.  - In case where an unsupported &#x60;sort&#x60; value is provided, the results will be sorted by the default (&#x60;-pk&#x60;). | [optional]
 **pageSize** | **float**| The maximum number of results to be returned per page | [optional] [default to 100]
 **cursor** | **string**| The cursor query string is used as the pivot value to filter results. If no value is provided, the service must return the first page. The value is Base64 encoded GET parameters, for example:   For a cursor string, there are 3 possible parameters to encode:     - &#x60;o&#x60;: Offset     - &#x60;r&#x60;: Reverse     - &#x60;p&#x60;: Position   Combine into GET parameters, for example: &#x60;r&#x3D;1&amp;p&#x3D;300&#x60;   Base 64 encoded it would become: &#x60;cj0xJnA9MzAw&#x60;   GET parameter in URL would be &#x60;https://some.url.com/api/endpoint/?cursor&#x3D;cj0xJnA9MzAw&#x60; | [optional]

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

Retrieving a specific order

This method allows to retrieve an order in particular

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

This method allows to update only specified fields of any order.

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
$orderPartialUpdate = {"id":"669","order_id":"555413","order_details":{"status":{"code":"fulfilled","message":"Fulfilled"},"tags":["october_campaign"]}}; // \Toppy\Sendcloud\Model\OrderPartialUpdate | Only set the fields you would like to update. If updating any of the `order_items`, `name` is required to match with the right `order_item`. If you need to add or remove items to an order, you have to update the whole order data through a POST request.

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
 **orderPartialUpdate** | [**\Toppy\Sendcloud\Model\OrderPartialUpdate**](../Model/OrderPartialUpdate.md)| Only set the fields you would like to update. If updating any of the &#x60;order_items&#x60;, &#x60;name&#x60; is required to match with the right &#x60;order_item&#x60;. If you need to add or remove items to an order, you have to update the whole order data through a POST request. | [optional]

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

Make a request to insert orders into Sendcloud API integrations. You can use multiple Sendcloud API Integrations within the same call.  ## Upsert Behavior This is an **upsert endpoint**, which means: - If an order with the same `order_id` and `integration.id` combination **already exists**, it will be **updated** - If no matching order exists, a **new order will be created** - **Optional**: You can include the Sendcloud `id` field to explicitly update a specific order   - **Important**: When returned in responses, `id` is an **integer**, but when sending it in requests, it must be a **string**   - Example: Response returns `\"id\": 669`, but request must send `\"id\": \"669\"`  ## Batch Processing - Process multiple orders in a single request (up to **100 orders maximum**) - Orders from different integrations can be included in the same batch - **All-or-nothing transaction**: If any order in the batch fails validation, the entire batch is rejected and zero orders are created or updated  ## Limitations and Constraints - **Maximum batch size**: 100 orders per request - **Upsert matching**: Orders are matched by the combination of `order_id` + `integration.id` - **Immutable fields**: When updating existing orders, certain fields like `order_id` cannot be changed - **Concurrent processing**: If the same `order_id` is being processed by another request, you'll receive a conflict error. Wait a moment and retry - **Integration access**: You can only create/update orders for integrations that belong to your account  ## Best Practices - Ensure all required fields are present before sending the request - Handle errors gracefully and implement retry logic for transient failures

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
$sendcloudPartnerId = 'sendcloudPartnerId_example'; // string | Send an additional request header for the system to recognize you if you are an official <a href=\"https://www.sendcloud.com/ecosystem/\" target=\"_blank\">**Sendcloud Tech Partner**</a>. Sendcloud Partner UUID is provided to Sendcloud partners. The provided partner UUID will only be inserted for new orders. Existing orders will not be updated.
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
 **sendcloudPartnerId** | **string**| Send an additional request header for the system to recognize you if you are an official &lt;a href&#x3D;\&quot;https://www.sendcloud.com/ecosystem/\&quot; target&#x3D;\&quot;_blank\&quot;&gt;**Sendcloud Tech Partner**&lt;/a&gt;. Sendcloud Partner UUID is provided to Sendcloud partners. The provided partner UUID will only be inserted for new orders. Existing orders will not be updated. | [optional]
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
