# # LabelAsync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipmentId** | **string** | The ID of the shipment that was created for the provided order. | [optional]
**orderId** | **string** | The ID of your order. | [optional]
**orderNumber** | **string** | A human-readable order number. | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](.md) |  | [optional]
**parcelId** | **int** | The ID of the parcel the label belongs to. For multicollo shipments, the ID of the first parcel will be returned.  **Deprecated** in favour of the &#x60;parcels_ids&#x60; field, which returns an array containing the parcel ID (or multiple parcel IDs for a multicollo shipment). | [optional]
**parcelsIds** | **int[]** | An array containing the IDs of all the parcels the labels belong to. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
