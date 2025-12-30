# # ParcelCommon

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dimensions** | [**\Toppy\Sendcloud\Model\StrDimensions**](StrDimensions.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\Model\StrWeight**](StrWeight.md) |  | [optional]
**additionalInsuredPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**labelNotes** | **string[]** | Custom messages printed on the shipping label. Use this field to include custom text - such as invoice numbers, product IDs, or internal reference codes - on the package’s shipping label.   **Note that support for label messages varies by carrier; some carriers may ignore this field or offer alternatives, such as delivery instructions, which are communicated to the carrier but not printed on the label. Some carriers may apply label notes at the shipment level rather than per individual parcel.** | [optional]
**sscc** | **string** |  | [optional]
**parcelItems** | [**\Toppy\Sendcloud\Model\ParcelItem[]**](ParcelItem.md) | List of items / products that the parcel contains. **Note that parcel items array is required for shipments that require customs documents.** | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
