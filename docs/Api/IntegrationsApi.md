# Toppy\Sendcloud\V3\IntegrationsApi

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scPublicV3IntegrationsDeleteDeleteIntegration()**](IntegrationsApi.md#scPublicV3IntegrationsDeleteDeleteIntegration) | **DELETE** /integrations/{id} | Delete an integration
[**scPublicV3IntegrationsGetListIntegrations()**](IntegrationsApi.md#scPublicV3IntegrationsGetListIntegrations) | **GET** /integrations | Retrieve a list of integrations
[**scPublicV3IntegrationsGetRetrieveIntegration()**](IntegrationsApi.md#scPublicV3IntegrationsGetRetrieveIntegration) | **GET** /integrations/{id} | Retrieve an integration
[**scPublicV3IntegrationsGetShopOrderStatuses()**](IntegrationsApi.md#scPublicV3IntegrationsGetShopOrderStatuses) | **GET** /shop-order-statuses | Retrieve shop order statuses for an integration
[**scPublicV3IntegrationsGetShopOrderStatusesMapping()**](IntegrationsApi.md#scPublicV3IntegrationsGetShopOrderStatusesMapping) | **GET** /shop-order-statuses/mapping | Retrieve custom status mapping for an integration
[**scPublicV3IntegrationsPatchUpdateIntegration()**](IntegrationsApi.md#scPublicV3IntegrationsPatchUpdateIntegration) | **PATCH** /integrations/{id} | Update certain parts of an integration
[**scPublicV3IntegrationsPostShopOrderStatuses()**](IntegrationsApi.md#scPublicV3IntegrationsPostShopOrderStatuses) | **POST** /shop-order-statuses | Create or overwrite shop order statuses
[**scPublicV3IntegrationsPostShopOrderStatusesMapping()**](IntegrationsApi.md#scPublicV3IntegrationsPostShopOrderStatusesMapping) | **POST** /shop-order-statuses/mapping | Create or update custom status mapping for an integration


## `scPublicV3IntegrationsDeleteDeleteIntegration()`

```php
scPublicV3IntegrationsDeleteDeleteIntegration($id)
```

Delete an integration

Safely delete one of your integrations from the Sendcloud system

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud integration ID

try {
    $apiInstance->scPublicV3IntegrationsDeleteDeleteIntegration($id);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsDeleteDeleteIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud integration ID |

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

## `scPublicV3IntegrationsGetListIntegrations()`

```php
scPublicV3IntegrationsGetListIntegrations($sort): \Toppy\Sendcloud\V3\Model\IntegrationListResponse
```

Retrieve a list of integrations

Retrieve all valid integrations from the Sendcloud system for a given user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$sort = updated_at; // string | Set the order for the response items: - Sorting is supported by the `integration_type`, `created_at`, `updated_at`, `last_fetch`, and `failing_since` attributes in the response object. - To sort the response in descending order, add the prefix `-` to the query param value. - By default, the items will be ordered by `last_fetch` and then `created_at`.

try {
    $result = $apiInstance->scPublicV3IntegrationsGetListIntegrations($sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsGetListIntegrations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **string**| Set the order for the response items: - Sorting is supported by the &#x60;integration_type&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;, &#x60;last_fetch&#x60;, and &#x60;failing_since&#x60; attributes in the response object. - To sort the response in descending order, add the prefix &#x60;-&#x60; to the query param value. - By default, the items will be ordered by &#x60;last_fetch&#x60; and then &#x60;created_at&#x60;. | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\IntegrationListResponse**](../Model/IntegrationListResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3IntegrationsGetRetrieveIntegration()`

```php
scPublicV3IntegrationsGetRetrieveIntegration($id): \Toppy\Sendcloud\V3\Model\IntegrationGetResponse
```

Retrieve an integration

Get a valid integration from the Sendcloud system

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud integration ID

try {
    $result = $apiInstance->scPublicV3IntegrationsGetRetrieveIntegration($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsGetRetrieveIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud integration ID |

### Return type

[**\Toppy\Sendcloud\V3\Model\IntegrationGetResponse**](../Model/IntegrationGetResponse.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3IntegrationsGetShopOrderStatuses()`

```php
scPublicV3IntegrationsGetShopOrderStatuses($integrationId, $language, $showDeleted): \Toppy\Sendcloud\V3\Model\GetShopOrderStatuses
```

Retrieve shop order statuses for an integration

Fetch all available shop order statuses for the Prestashop v2 integration, in the default or selected language.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$integrationId = 251; // int | Filter response on `integration_id`.
$language = en-gb; // string | Get a response for the specified language.
$showDeleted = true; // bool | Get all currently available and historical statuses.

try {
    $result = $apiInstance->scPublicV3IntegrationsGetShopOrderStatuses($integrationId, $language, $showDeleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsGetShopOrderStatuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **integrationId** | **int**| Filter response on &#x60;integration_id&#x60;. |
 **language** | **string**| Get a response for the specified language. | [optional]
 **showDeleted** | **bool**| Get all currently available and historical statuses. | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\GetShopOrderStatuses**](../Model/GetShopOrderStatuses.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3IntegrationsGetShopOrderStatusesMapping()`

```php
scPublicV3IntegrationsGetShopOrderStatusesMapping($integrationId): \Toppy\Sendcloud\V3\Model\GetCustomStatusMapping
```

Retrieve custom status mapping for an integration

Fetch a map of available shop order statuses and Sendcloud's internal status category for the integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$integrationId = 251; // int | Filter response on `integration_id`.

try {
    $result = $apiInstance->scPublicV3IntegrationsGetShopOrderStatusesMapping($integrationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsGetShopOrderStatusesMapping: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **integrationId** | **int**| Filter response on &#x60;integration_id&#x60;. |

### Return type

[**\Toppy\Sendcloud\V3\Model\GetCustomStatusMapping**](../Model/GetCustomStatusMapping.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3IntegrationsPatchUpdateIntegration()`

```php
scPublicV3IntegrationsPatchUpdateIntegration($id, $integrationModel)
```

Update certain parts of an integration

Update the shop name, shop URL, service point settings, webhook settings, and feedback type of an integration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Filtering on the Sendcloud integration ID
$integrationModel = {"shop_name":"My Webshop"}; // \Toppy\Sendcloud\V3\Model\IntegrationModel

try {
    $apiInstance->scPublicV3IntegrationsPatchUpdateIntegration($id, $integrationModel);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsPatchUpdateIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Filtering on the Sendcloud integration ID |
 **integrationModel** | [**\Toppy\Sendcloud\V3\Model\IntegrationModel**](../Model/IntegrationModel.md)|  | [optional]

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

## `scPublicV3IntegrationsPostShopOrderStatuses()`

```php
scPublicV3IntegrationsPostShopOrderStatuses($postShopOrderStatuses): Null
```

Create or overwrite shop order statuses

Insert shop-specific custom statuses into the Sendcloud system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$postShopOrderStatuses = {"integration_id":23452345,"statuses":[{"external_id":"Send-4","translations":[{"status":"Sent","language":"en-gb"},{"status":"Verzonden","language":"nl-nl"}]},{"external_id":"15","translations":[{"status":"Delivered","language":"en-gb"},{"status":"Bezorgt","language":"nl-nl"}]}]}; // \Toppy\Sendcloud\V3\Model\PostShopOrderStatuses

try {
    $result = $apiInstance->scPublicV3IntegrationsPostShopOrderStatuses($postShopOrderStatuses);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsPostShopOrderStatuses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **postShopOrderStatuses** | [**\Toppy\Sendcloud\V3\Model\PostShopOrderStatuses**](../Model/PostShopOrderStatuses.md)|  | [optional]

### Return type

[**Null**](../Model/Null.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scPublicV3IntegrationsPostShopOrderStatusesMapping()`

```php
scPublicV3IntegrationsPostShopOrderStatusesMapping($createCustomStatusMapping): Null
```

Create or update custom status mapping for an integration

Upsert a map of available shop order statuses and Sendcloud's internal status category for an integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$createCustomStatusMapping = {"integration_id":23452345,"mapping":[{"status_category":"READY_TO_SEND","external_id":"11"},{"status_category":"IN_TRANSIT","external_id":"11"},{"status_category":"DELIVERED","external_id":"12"},{"status_category":"CANCEL","external_id":null}]}; // \Toppy\Sendcloud\V3\Model\CreateCustomStatusMapping

try {
    $result = $apiInstance->scPublicV3IntegrationsPostShopOrderStatusesMapping($createCustomStatusMapping);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->scPublicV3IntegrationsPostShopOrderStatusesMapping: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createCustomStatusMapping** | [**\Toppy\Sendcloud\V3\Model\CreateCustomStatusMapping**](../Model/CreateCustomStatusMapping.md)|  | [optional]

### Return type

[**Null**](../Model/Null.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
