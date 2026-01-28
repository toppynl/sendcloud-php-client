# # DhlParcelGbPickupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeSlots** | [**\ToppySendcloudV3ModelTimeSlot[]**](TimeSlot.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. |
**items** | [**\Toppy\Sendcloud\V3\Model\BasePickupItem[]**](BasePickupItem.md) | Items scheduled to be picked up. | [optional]
**reference** | **string** | Reference number for your administration. | [optional]
**specialInstructions** | **string** | Special instructions for the pickup driver. | [optional]
**carrierCode** | **string** | Pickup carrier code selected by the user. |
**contractId** | **int** | Contract ID you want to use for the pickup request. | [optional]
**address** | [**\Toppy\Sendcloud\V3\Model\PickupAddress**](PickupAddress.md) |  |
**customerAccountNumber** | **string** | Customer number (CUS) |
**tradingLocationId** | **string** | Unique ID for customer trading location |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
