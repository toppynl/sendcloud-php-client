# # ParcelTrackingParcelTrackingCreateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**announcedAt** | **\DateTime** | The timestamp of when the parcel was announced to the carrier (label was created) |
**createdAt** | **\DateTime** | The timestamp of when the parcel was created in the system |
**details** | [**\Toppy\Sendcloud\V3\Model\ParcelDetailResponse**](ParcelDetailResponse.md) |  |
**fromAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**parcelItems** | [**\Toppy\Sendcloud\V3\Model\ParcelItemWithSourceId[]**](ParcelItemWithSourceId.md) | List of items / products that the parcel contains | [optional]
**shipWith** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingShipWith**](ParcelTrackingShipWith.md) |  |
**sourceId** | **string** | An external identifier that clients can provide to link the parcel with the corresponding record in their own system |
**toAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**trackingNumbers** | [**\Toppy\Sendcloud\V3\Model\TrackingNumberResponse[]**](TrackingNumberResponse.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
