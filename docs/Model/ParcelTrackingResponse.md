# # ParcelTrackingResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**announcedAt** | **\DateTime** | The timestamp of when the parcel was announced to the carrier (label was created) |
**createdAt** | **\DateTime** | The timestamp of when the parcel was created in the system |
**details** | [**\Toppy\Sendcloud\V3\Model\ParcelDetailResponse**](ParcelDetailResponse.md) |  |
**events** | [**\Toppy\Sendcloud\V3\Model\ParcelEventResponse[]**](ParcelEventResponse.md) |  |
**fromAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**parcelItems** | [**\Toppy\Sendcloud\V3\Model\ParcelItemWithSourceId[]**](ParcelItemWithSourceId.md) | List of items / products that the parcel contains | [optional]
**shipWith** | [**\Toppy\Sendcloud\V3\Model\ShipWith**](ShipWith.md) |  | [optional]
**sourceId** | **string** | An external identifier that clients can provide to link the parcel with the corresponding record in their own system |
**toAddress** | [**\Toppy\Sendcloud\V3\Model\ParcelTrackingAddress**](ParcelTrackingAddress.md) |  |
**trackingNumbers** | [**\Toppy\Sendcloud\V3\Model\TrackingNumberResponse[]**](TrackingNumberResponse.md) |  |
**updatedAt** | **\DateTime** | The timestamp of when the parcel was last updated in the system. Only altered by updates on &#x60;announced_at&#x60;, &#x60;contract&#x60;, and &#x60;source_id&#x60; |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
