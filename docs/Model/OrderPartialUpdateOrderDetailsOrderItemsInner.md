# # OrderPartialUpdateOrderDetailsOrderItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemId** | **string** | Order Item external ID in shop system | [optional]
**productId** | **string** | Shop system product ID | [optional]
**name** | **string** | The name of ordered product | [optional]
**description** | **string** | The product description | [optional]
**quantity** | **int** |  | [optional]
**sku** | **string** | Stock keeping unit - used by retailers to assign to products, in order to keep track of stock levels internally. | [optional]
**hsCode** | **string** |  | [optional]
**countryOfOrigin** | **string** | Country code of origin of the item in ISO 3166-1 alpha-2 | [optional]
**properties** | **array<string,mixed>** | Any custom user-defined properties of order item or product | [optional]
**unitPrice** | [**\Toppy\Sendcloud\V3\Model\Price**](Price.md) |  | [optional]
**totalPrice** | [**\Toppy\Sendcloud\V3\Model\Price**](Price.md) |  | [optional]
**measurement** | [**\Toppy\Sendcloud\V3\Model\Measurement**](Measurement.md) |  | [optional]
**midCode** | **string** | MID code, an abbreviation for Manufacturer&#39;s Identification code, is necessary on the commercial invoice, serving as an alternative for the complete manufacturer, shipper, or exporter details, and it&#39;s mandatory for U.S. formal customs entries. | [optional]
**materialContent** | **string** | A description of materials of the order content. | [optional]
**intendedUse** | **string** | Intended use of the order contents: personal or commercial. | [optional]
**deliveryDates** | [**\Toppy\Sendcloud\V3\Model\OrderPartialUpdateOrderDetailsOrderItemsInnerDeliveryDates**](OrderPartialUpdateOrderDetailsOrderItemsInnerDeliveryDates.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
