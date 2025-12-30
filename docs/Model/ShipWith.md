# # ShipWith

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The way the shipping method and carrier will be selected. The default is &#x60;shipping_product_code&#x60;,  but the &#x60;shipping_option_code&#x60; is a new and the preferred way. | [optional] [default to 'shipping_product_code']
**shippingOptionCode** | **string** | Shipping option code as provided by the [shipping options API](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipping-options/operations/create-a-fetch-shipping-option)  and the &#x60;code&#x60; property of the corresponding response. Required if &#x60;type&#x60; is &#x60;shipping_option_code&#x60;. | [optional]
**shippingProductCode** | **string** | Shipping product code as provided by the [shipping products API](https://api.sendcloud.dev/docs/sendcloud-public-api/shipping-products/operations/list-shipping-products) and the &#x60;code&#x60; property of the corresponding response. Required if &#x60;type&#x60; is &#x60;shipping_product_code&#x60;. | [optional]
**functionalities** | [**\Toppy\Sendcloud\Model\CarrierShippingFunctionalities**](CarrierShippingFunctionalities.md) |  | [optional]
**contract** | **int** | ID of the contract to ship the return with | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
