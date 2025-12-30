# # ScPublicV3ScpGetPickup200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeSlots** | [**\ToppySendcloudModelTimeSlotEndAtRequired[]**](TimeSlotEndAtRequired.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. | [optional]
**items** | [**\Toppy\Sendcloud\Model\UpsPickupItem[]**](UpsPickupItem.md) |  | [optional]
**reference** | **string** | Reference number for your administration. | [optional]
**specialInstructions** | **string** | Special instructions for the pickup driver. | [optional]
**carrierCode** | **string** | Pickup carrier code selected by the user. |
**contractId** | **int** | Id of the contract that is used to create the pickup. | [optional]
**address** | [**\Toppy\Sendcloud\Model\PickupAddressPhoneNumberRequired**](PickupAddressPhoneNumberRequired.md) |  |
**id** | **int** | Unique identifier of the pickup. | [optional]
**trackingNumber** | **string** |  | [optional]
**status** | **string** |  | [optional]
**createdAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is created. | [optional]
**cancelledAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is cancelled. | [optional]
**originDetail** | [**\Toppy\Sendcloud\Model\FedexOriginDetail**](FedexOriginDetail.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
