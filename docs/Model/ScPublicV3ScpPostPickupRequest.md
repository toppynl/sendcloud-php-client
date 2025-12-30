# # ScPublicV3ScpPostPickupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeSlots** | [**\ToppySendcloudModelTimeSlotEndAtRequired[]**](TimeSlotEndAtRequired.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. |
**items** | [**\Toppy\Sendcloud\Model\UpsPickupItem[]**](UpsPickupItem.md) |  | [optional]
**reference** | **string** | Reference number for your administration. | [optional]
**specialInstructions** | **string** | Special instructions for the pickup driver. | [optional]
**carrierCode** | **string** | Pickup carrier code selected by the user. |
**contractId** | **int** | Contract ID you want to use for the pickup request. | [optional]
**address** | [**\Toppy\Sendcloud\Model\UpsPickupAddress**](UpsPickupAddress.md) |  |
**customerAccountNumber** | **string** | Customer number (CUS) |
**tradingLocationId** | **string** | Unique ID for customer trading location |
**originDetail** | [**\Toppy\Sendcloud\Model\FedexOriginDetail**](FedexOriginDetail.md) |  |
**isOverweight** | **bool** | Indicates if at least any package is over 70 lbs or 32 kgs. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
