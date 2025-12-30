# # LabelAsync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipmentId** | **string** | ID of the shipment that was created for the provided order. | [optional]
**orderId** | **string** | ID of your order. | [optional]
**orderNumber** | **string** | Human readable order number. | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](.md) |  | [optional]
**parcelId** | **int** | ID of the parcel the label belongs to. In case of multicollo shipment ID of the first parcel will be returned. **Deprecated** in favour of the &#x60;parcel_ids&#x60; field, that provides IDs of all parcels when used with multicollo. | [optional]
**parcelsIds** | **int[]** | A list with IDs of all the parcels the labels belong to | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
