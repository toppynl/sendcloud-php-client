# Toppy\Sendcloud\V3\OrdersApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

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
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OrdersApi(
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
scPublicV3OrdersGetListOrders(): \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersGetListOrders200Response
```

Retrieve a list of orders

Get a list of orders filtered by integration, order number, order ID, order status, creation date, and update date. You can also optionally sort the results and pass a `cursor` value.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->scPublicV3OrdersGetListOrders();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersGetListOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersGetListOrders200Response**](../Model/ScPublicV3OrdersGetListOrders200Response.md)

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
scPublicV3OrdersGetRetrieveOrder($id): \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersGetRetrieveOrder200Response
```

Retrieve an order

Find a specific order by its order ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OrdersApi(
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

[**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersGetRetrieveOrder200Response**](../Model/ScPublicV3OrdersGetRetrieveOrder200Response.md)

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
scPublicV3OrdersPatchPartialUpdateOrder($id, $orderPartialUpdate)
```

Update an order

Partially update some fields of an order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud order ID
$orderPartialUpdate = {"id":"669","order_id":"555413","order_details":{"status":{"code":"fulfilled","message":"Fulfilled"},"tags":["october_campaign"]}}; // \Toppy\Sendcloud\V3\Model\OrderPartialUpdate | Only include the fields you would like to update. If you need to update any of the `order_items`, the `name` field is required so that the correct `order_item` is updated. If you need to add items to or remove items from an order, you should use the [Create/Update orders in batch](/api/v3/orders/create-update-orders-in-batch) endpoint instead.

try {
    $apiInstance->scPublicV3OrdersPatchPartialUpdateOrder($id, $orderPartialUpdate);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersPatchPartialUpdateOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud order ID |
 **orderPartialUpdate** | [**\Toppy\Sendcloud\V3\Model\OrderPartialUpdate**](../Model/OrderPartialUpdate.md)| Only include the fields you would like to update. If you need to update any of the &#x60;order_items&#x60;, the &#x60;name&#x60; field is required so that the correct &#x60;order_item&#x60; is updated. If you need to add items to or remove items from an order, you should use the [Create/Update orders in batch](/api/v3/orders/create-update-orders-in-batch) endpoint instead. | [optional]

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

## `scPublicV3OrdersPostCreateOrders()`

```php
scPublicV3OrdersPostCreateOrders($scPublicV3OrdersPostCreateOrdersRequestInner): \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersPostCreateOrders201Response
```

Create/Update orders in batch

Use this endpoint to insert orders into a Sendcloud API integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$scPublicV3OrdersPostCreateOrdersRequestInner = [{"order_id":"555413","order_number":"OXSDFGHTD-12","order_details":{"integration":{"id":7},"status":{"code":"fulfilled","message":"Fulfilled"},"order_created_at":"2018-02-27T10:00:00.556Z","order_items":[{"name":"Cylinder candle","quantity":1,"total_price":{"value":3.5,"currency":"EUR"}}]},"payment_details":{"total_price":{"value":3.5,"currency":"EUR"},"status":{"code":"paid","message":"Paid"}},"shipping_address":{"name":"John Doe","address_line_1":"Lansdown Glade","house_number":"15","postal_code":"5341XT","city":"Oss","country_code":"NL"},"shipping_details":{"is_local_pickup":false,"delivery_indicator":"DHL home delivery","measurement":{"weight":{"value":3,"unit":"kg"}}}}]; // \Toppy\Sendcloud\V3\Model\ScPublicV3OrdersPostCreateOrdersRequestInner[]

try {
    $result = $apiInstance->scPublicV3OrdersPostCreateOrders($scPublicV3OrdersPostCreateOrdersRequestInner);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->scPublicV3OrdersPostCreateOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scPublicV3OrdersPostCreateOrdersRequestInner** | [**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersPostCreateOrdersRequestInner[]**](../Model/ScPublicV3OrdersPostCreateOrdersRequestInner.md)|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\ScPublicV3OrdersPostCreateOrders201Response**](../Model/ScPublicV3OrdersPostCreateOrders201Response.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
