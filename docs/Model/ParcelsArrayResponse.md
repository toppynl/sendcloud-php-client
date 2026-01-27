# # ParcelsArrayResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dimensions** | [**\Toppy\Sendcloud\Model\StrDimensions**](StrDimensions.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\Model\StrWeight**](StrWeight.md) |  | [optional]
**additionalInsuredPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**labelNotes** | **string[]** | Custom messages printed on the shipping label. Use this field to include custom text - such as invoice numbers, product IDs, or internal reference codes - on the package’s shipping label. | [optional]
**sscc** | **string** | The Serial Shipping Container Code (SSCC) serves as a globally unique identifier for a logistic unit, functioning as a digital \&quot;license plate\&quot; for tracking and managing goods throughout the supply chain. | [optional]
**parcelItems** | [**\Toppy\Sendcloud\Model\ParcelItem[]**](ParcelItem.md) | List of items/products that the parcel contains. **Note that parcel items array is required for shipments that require customs documents.** | [optional]
**createdAt** | **\DateTime** | The timestamp of when the parcel was created | [optional] [readonly]
**updatedAt** | **\DateTime** | The timestamp of when the parcel was last updated | [optional] [readonly]
**announcedAt** | **\DateTime** | The timestamp of when the parcel was announced to the carrier (label was created) | [optional] [readonly]
**id** | **int** | ID of the parcel (required to retrieve a parcel document for async announcement) | [optional] [readonly]
**status** | [**\Toppy\Sendcloud\Model\Status**](Status.md) |  | [optional]
**documents** | [**\Toppy\Sendcloud\Model\Documents[]**](Documents.md) | An array of documents. A parcel can contain multiple documents, for instance labels and a customs form. This field returns an array of all the available documents for this parcel. | [optional] [readonly]
**trackingNumber** | **string** | Tracking number of the shipment. | [optional] [readonly]
**trackingUrl** | **string** | Tracking url of this shipment. | [optional] [readonly]
**additionalCarrierData** | [**\Toppy\Sendcloud\Model\CarrierSpecificData**](CarrierSpecificData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
