# # HermesDePickupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeSlots** | [**\ToppySendcloudModelTimeSlotEndAtRequired[]**](TimeSlotEndAtRequired.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. | [optional]
**items** | [**\Toppy\Sendcloud\Model\BasePickupItem[]**](BasePickupItem.md) | Items scheduled to be picked up. | [optional]
**reference** | **string** | Reference number for your administration. | [optional]
**specialInstructions** | **string** | Special instructions for the pickup driver. | [optional]
**carrierCode** | **string** | Pickup carrier code selected by the user. |
**contractId** | **int** | Contract ID you want to use for the pickup request. | [optional]
**address** | [**\Toppy\Sendcloud\Model\PickupAddress**](PickupAddress.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
