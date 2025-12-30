# # ParcelTrackingCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**announcedAt** | **\DateTime** | The timestamp of when the parcel was announced to the carrier (label was created) |
**details** | [**\Toppy\Sendcloud\Model\ParcelDetailCreateRequest**](ParcelDetailCreateRequest.md) |  | [optional]
**fromAddress** | [**\Toppy\Sendcloud\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**insurance** | [**\Toppy\Sendcloud\Model\Insurance**](Insurance.md) |  | [optional]
**parcelItems** | [**\Toppy\Sendcloud\Model\ParcelItem[]**](ParcelItem.md) | List of items / products that the parcel contains | [optional]
**measurements** | [**\Toppy\Sendcloud\Model\Measurement**](Measurement.md) |  | [optional]
**returnPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](ShipWith.md) |  |
**shipment** | [**\Toppy\Sendcloud\Model\ShipmentCreateRequest**](ShipmentCreateRequest.md) |  |
**sourceId** | **string** | An external identifier that clients can provide to link the parcel with the corresponding record in their own system |
**toAddress** | [**\Toppy\Sendcloud\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**trackingNumber** | [**\Toppy\Sendcloud\Model\TrackingNumberCreateRequest**](TrackingNumberCreateRequest.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
