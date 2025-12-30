# # DhlDePickupResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique identifier of the pickup. | [optional]
**carrierCode** | **string** | Pickup carrier code selected by the user. | [optional]
**timeSlots** | [**\ToppySendcloudModelTimeSlot[]**](TimeSlot.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. | [optional]
**items** | [**\Toppy\Sendcloud\Model\DhlDePickupItem[]**](DhlDePickupItem.md) |  | [optional]
**reference** | **string** | Reference number for your administration. | [optional]
**specialInstructions** | **string** | Special instructions for the pickup driver. | [optional]
**trackingNumber** | **string** |  | [optional]
**status** | **string** |  | [optional]
**createdAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is created. | [optional]
**cancelledAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is cancelled. | [optional]
**contractId** | **int** | Id of the contract that is used to create the pickup. | [optional]
**address** | [**\Toppy\Sendcloud\Model\PickupAddress**](PickupAddress.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
