# Toppy\Sendcloud\V3\OAuth2Api

All URIs are relative to https://panel.sendcloud.sc/api/v3.

Method | HTTP request | Description
------------- | ------------- | -------------
[**oAuth2TokenExchange()**](OAuth2Api.md#oAuth2TokenExchange) | **POST** /oauth2/token | OAuth 2.0 token


## `oAuth2TokenExchange()`

```php
oAuth2TokenExchange($grantType, $clientId, $code, $redirectUri, $refreshToken): \Toppy\Sendcloud\V3\Model\OAuth2TokenExchange
```

OAuth 2.0 token

Use this endpoint to get a new OAuth 2.0 access token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\OAuth2Api(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$grantType = 'grantType_example'; // string
$clientId = 'clientId_example'; // string
$code = 'code_example'; // string
$redirectUri = 'redirectUri_example'; // string
$refreshToken = 'refreshToken_example'; // string

try {
    $result = $apiInstance->oAuth2TokenExchange($grantType, $clientId, $code, $redirectUri, $refreshToken);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuth2Api->oAuth2TokenExchange: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grantType** | **string**|  |
 **clientId** | **string**|  | [optional]
 **code** | **string**|  | [optional]
 **redirectUri** | **string**|  | [optional]
 **refreshToken** | **string**|  | [optional]

### Return type

[**\Toppy\Sendcloud\V3\Model\OAuth2TokenExchange**](../Model/OAuth2TokenExchange.md)

### Authorization

[HTTPBasicAuth](../../README.md#HTTPBasicAuth)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
