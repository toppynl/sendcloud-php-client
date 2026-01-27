# # ScPublicV3OrdersPostCreateOrdersRequestInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Sendcloud&#39;s internal ID for the order.  - In **responses**: Returned as an integer (e.g., &#x60;669&#x60;) - In **requests**: Optional field for explicitly updating a specific order. Must be provided as a string (e.g., &#x60;\&quot;669\&quot;&#x60;) - If omitted in requests, the upsert logic uses the combination of &#x60;order_id&#x60; + &#x60;integration.id&#x60; to match existing orders | [optional]
**orderId** | **string** | External order ID assigned by shop system |
**orderNumber** | **string** | Unique order number generated manually or by shop system |
**createdAt** | **\DateTime** | The date when an order was created at Sendcloud in ISO 8601 | [optional] [readonly]
**modifiedAt** | **\DateTime** | The date when an order was last modified at Sendcloud in ISO 8601 | [optional] [readonly]
**orderDetails** | [**\Toppy\Sendcloud\Model\OrderOrderDetails**](OrderOrderDetails.md) |  |
**paymentDetails** | [**\Toppy\Sendcloud\Model\PaymentDetails**](PaymentDetails.md) |  |
**customsDetails** | [**\Toppy\Sendcloud\Model\CustomsDetails**](CustomsDetails.md) |  | [optional]
**customerDetails** | [**\Toppy\Sendcloud\Model\CustomerDetails**](CustomerDetails.md) |  | [optional]
**billingAddress** | [**\Toppy\Sendcloud\Model\Address**](Address.md) |  | [optional]
**shippingAddress** | [**\Toppy\Sendcloud\Model\Address**](Address.md) |  | [optional]
**shippingDetails** | [**\Toppy\Sendcloud\Model\ShippingDetails**](ShippingDetails.md) |  | [optional]
**servicePointDetails** | [**\Toppy\Sendcloud\Model\ServicePoint**](ServicePoint.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
