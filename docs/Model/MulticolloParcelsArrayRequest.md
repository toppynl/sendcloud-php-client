# # MulticolloParcelsArrayRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parcels** | [**\Toppy\Sendcloud\V3\Model\ParcelCommon[]**](ParcelCommon.md) | Represent each package of the shipment.  There is a restriction to a maximum number of percels per shipment.   * **sync** announcements : max 15 parcels per shipment * **async** announcements: max 50 parcels per shipment  Note: each carrier can have a lower than the max number of parcels limit per shipment. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
