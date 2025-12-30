# # ListPickupResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Unique identifier of the pickup. | [optional]
**carrierCode** | **string** |  | [optional]
**country** | **string** | ISO 3166-1 alpha-2 country code. | [optional]
**trackingNumber** | **string** |  | [optional]
**timeSlots** | [**\ToppySendcloudModelTimeSlot[]**](TimeSlot.md) | Scheduled time slots for the pickup. Note that most carriers only support a single time slot. | [optional]
**status** | **string** |  | [optional]
**createdAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is created. | [optional]
**cancelledAt** | **\DateTime** | ISO 8601 DateTime at which the pickup is cancelled. | [optional]
**contractId** | **int** | Id of the contract that is used to create the pickup. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
