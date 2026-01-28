# # ParcelItemWithOptionalFields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**itemId** | **string** | Order Item external ID in shop system | [optional]
**description** | **string** | Description of the item | [optional]
**quantity** | **int** | Quantity of items shipped |
**weight** | [**\Toppy\Sendcloud\V3\Model\ShipmentsWeight**](ShipmentsWeight.md) |  | [optional]
**price** | [**\Toppy\Sendcloud\V3\Model\RequiredPrice**](RequiredPrice.md) |  | [optional]
**hsCode** | **string** | Harmonized System Code. **This field is required if it&#39;s an international shipment** | [optional]
**originCountry** | **string** | ISO-2 code of the country where the items were originally produced. **This field is required if it&#39;s an international shipment** | [optional]
**sku** | **string** | The SKU of the product | [optional]
**productId** | **string** | The internal ID of the product | [optional]
**midCode** | **string** | MID code is short for Manufacturer&#39;s Identification code and must be shown on the commercial invoice. It&#39;s used as an alternative to the full name and address of a manufacturer, shipper or exporter and is always required for U.S. formal customs entries. | [optional]
**materialContent** | **string** | A description of materials of the order content. | [optional]
**intendedUse** | **string** | Intended use of the order contents. The intended use may be personal or commercial. | [optional]
**dangerousGoods** | [**\Toppy\Sendcloud\V3\Model\DangerousGoods**](DangerousGoods.md) |  | [optional]
**ddsReference** | **string** | The DDS (Due Diligence Statement) reference number associated with the item, if applicable. See EUDR system for more details. | [optional]
**taricDocCode** | **string** | TARIC document codes are specific alphanumeric codes used in EU customs declarations (Box 44) to identify required supporting documents, certificates, or conditions for a product, like health certificates (e.g., 3200), origin proofs (e.g., EUR.1), or special authorizations (e.g., C716 for due diligence) for simplified procedures, ensuring compliance with EU trade rules for various goods. | [optional]
**properties** | **array<string,mixed>** | Any custom user-defined properties of order item or product | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
