# # PaymentDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**isCashOnDelivery** | **bool** | Indicates if customers will pay the full order amount upon delivery of the order | [optional]
**totalPrice** | [**\Toppy\Sendcloud\V3\Model\OrdersPrice**](OrdersPrice.md) |  |
**subtotalPrice** | [**\Toppy\Sendcloud\V3\Model\OrdersPrice**](OrdersPrice.md) |  | [optional]
**estimatedShippingPrice** | [**\Toppy\Sendcloud\V3\Model\OrdersPrice**](OrdersPrice.md) |  | [optional]
**estimatedTaxPrice** | [**\Toppy\Sendcloud\V3\Model\OrdersPrice**](OrdersPrice.md) |  | [optional]
**status** | [**\Toppy\Sendcloud\V3\Model\PaymentDetailsStatus**](PaymentDetailsStatus.md) |  |
**invoiceDate** | **string** | The date when invoice was issued. | [optional]
**discountGranted** | [**\Toppy\Sendcloud\V3\Model\CostsObject**](.md) |  | [optional]
**insuranceCosts** | [**\Toppy\Sendcloud\V3\Model\CostsObject**](.md) |  | [optional]
**freightCosts** | [**\Toppy\Sendcloud\V3\Model\CostsObject**](.md) |  | [optional]
**otherCosts** | [**\Toppy\Sendcloud\V3\Model\CostsObject**](.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
