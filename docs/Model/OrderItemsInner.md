# # OrderItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemId** | **string** | Order Item external ID in shop system | [optional]
**productId** | **string** | Shop system product ID | [optional]
**variantId** | **string** | Shop system variant ID of the product | [optional]
**imageUrl** | **string** | A url to an image representing the given product (or variation of the product if applicable). When providing &#x60;image_url&#x60; the &#x60;product_id&#x60; is required for image to be correctly displayed. | [optional]
**name** | **string** | The name of ordered product |
**description** | **string** | The product description | [optional]
**quantity** | **int** | The quantity field on an order item represents the number of units of a product a customer has ordered. |
**sku** | **string** | Stock keeping unit - used by retailers to assign to products, in order to keep track of stock levels internally. | [optional]
**hsCode** | **string** | The Harmonized System (HS) code is a standardized numerical system used to classify traded products in international commerce | [optional]
**countryOfOrigin** | **string** | Country code of origin of the item in ISO 3166-1 alpha-2 | [optional]
**properties** | **array<string,mixed>** | Any custom user-defined properties of order item or product | [optional]
**unitPrice** | [**\Toppy\Sendcloud\V3\Model\Price**](Price.md) |  | [optional]
**totalPrice** | [**\Toppy\Sendcloud\V3\Model\Price**](Price.md) |  |
**measurement** | [**\Toppy\Sendcloud\V3\Model\Measurement**](Measurement.md) |  | [optional]
**ean** | **string** | European standardised number for an article, EAN-13 | [optional]
**deliveryDates** | [**\Toppy\Sendcloud\V3\Model\DeliveryDates**](DeliveryDates.md) |  | [optional]
**midCode** | **string** | MID code is short for Manufacturer&#39;s Identification code and must be shown on the commercial invoice. It&#39;s used as an alternative to the full name and address of a manufacturer, shipper or exporter and is always required for U.S. formal customs entries. | [optional]
**materialContent** | **string** | A description of materials of the order content. | [optional]
**intendedUse** | **string** | Intended use of the order contents. The intended use may be personal or commercial. | [optional]
**dangerousGoods** | [**\Toppy\Sendcloud\V3\Model\DangerousGoods**](DangerousGoods.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
