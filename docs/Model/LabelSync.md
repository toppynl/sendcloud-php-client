# # LabelSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipmentId** | **string** | ID of the shipment that was created for the provided order. | [optional]
**orderId** | **string** | ID of your order. | [optional]
**orderNumber** | **string** | Human readable order number. | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](.md) |  | [optional]
**parcelId** | **int** | ID of the parcel the label belongs to. | [optional]
**labelDetails** | [**\Toppy\Sendcloud\Model\LabelSyncAllOfLabelDetails**](LabelSyncAllOfLabelDetails.md) |  | [optional]
**documents** | [**\Toppy\Sendcloud\Model\Documents[]**](Documents.md) | An array of documents. A parcel can contain multiple documents, for instance labels and a customs form. This field returns an array of all the available documents for this parcel. | [optional] [readonly]
**trackingNumber** | **string** | Tracking number of the shipment. | [optional] [readonly]
**trackingUrl** | **string** | Tracking url of this shipment. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
