# # LabelSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipmentId** | **string** | The ID of the shipment that was created for the provided order. | [optional]
**orderId** | **string** | The ID of your order. | [optional]
**orderNumber** | **string** | A human-readable order number. | [optional]
**shipWith** | [**\Toppy\Sendcloud\V3\Model\ShipWith**](.md) |  | [optional]
**parcelId** | **int** | The ID of the parcel the label belongs to. | [optional]
**labelDetails** | [**\Toppy\Sendcloud\V3\Model\LabelSyncAllOfLabelDetails**](LabelSyncAllOfLabelDetails.md) |  | [optional]
**documents** | [**\Toppy\Sendcloud\V3\Model\Documents[]**](Documents.md) | An array of documents. A parcel can contain multiple documents, for instance labels and a customs form. This field returns an array of all the available documents for this parcel. | [optional] [readonly]
**trackingNumber** | **string** | Tracking number of the shipment. | [optional] [readonly]
**trackingUrl** | **string** | Tracking url of this shipment. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
