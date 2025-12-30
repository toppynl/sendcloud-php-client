# # ParcelItemReturnsCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemId** | **string** | Order Item external ID in shop system | [optional]
**description** | **string** | Description of the item | [optional]
**quantity** | **int** | Quantity of items shipped | [optional]
**weight** | [**\Toppy\Sendcloud\Model\Weight**](Weight.md) |  | [optional]
**price** | [**\Toppy\Sendcloud\Model\PriceWithAnyCurrency**](PriceWithAnyCurrency.md) |  | [optional]
**value** | [**\Toppy\Sendcloud\Model\PriceWithAnyCurrency**](PriceWithAnyCurrency.md) |  | [optional]
**hsCode** | **string** | Harmonized System Code. **This field is required if it&#39;s an international return** | [optional]
**originCountry** | **string** | ISO-2 code of the country where the items were originally produced. **This field is required if it&#39;s an international return** | [optional]
**sku** | **string** | The SKU of the product | [optional]
**productId** | **string** | The internal ID of the product | [optional]
**returnReasonId** | **string** | The ID of the return reason, if any. | [optional]
**returnMessage** | **string** | Extra information relating to the return reason | [optional]
**midCode** | **string** | MID code is short for Manufacturer&#39;s Identification code and must be shown on the commercial invoice.  It&#39;s used as an alternative to the full name and address of a manufacturer, shipper or exporter  and is always required for U.S. formal customs entries. | [optional]
**materialContent** | **string** | A description of materials of the order content. | [optional]
**intendedUse** | **string** | Intended use of the order contents. The intended use may be personal or commercial. | [optional]
**properties** | **array<string,mixed>** | Any custom user-defined properties of order item or product | [optional]
**variantId** | **string** | Variant ID of the product. Imported from a shop system | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
