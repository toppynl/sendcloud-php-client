# # ParcelTrackingCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**announcedAt** | **\DateTime** | The timestamp of when the parcel was announced to the carrier (label was created) |
**details** | [**\Toppy\Sendcloud\V3\Model\ParcelDetailCreateRequest**](ParcelDetailCreateRequest.md) |  | [optional]
**fromAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**insurance** | [**\Toppy\Sendcloud\V3\Model\Insurance**](Insurance.md) |  | [optional]
**parcelItems** | [**\Toppy\Sendcloud\V3\Model\ParcelItem[]**](ParcelItem.md) | List of items / products that the parcel contains | [optional]
**measurements** | [**\Toppy\Sendcloud\V3\Model\Measurement**](Measurement.md) |  | [optional]
**returnPrice** | [**\Toppy\Sendcloud\V3\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**shipWith** | [**\Toppy\Sendcloud\V3\Model\ShipWith**](ShipWith.md) |  |
**shipment** | [**\Toppy\Sendcloud\V3\Model\ShipmentCreateRequest**](ShipmentCreateRequest.md) |  |
**sourceId** | **string** | An external identifier that clients can provide to link the parcel with the corresponding record in their own system |
**toAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**trackingNumber** | [**\Toppy\Sendcloud\V3\Model\TrackingNumberCreateRequest**](TrackingNumberCreateRequest.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
