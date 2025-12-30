# # IntegrationModel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shopName** | **string** | Name of the shop. | [optional]
**shopUrl** | **string** | URL of the shop the integration connects to. | [optional]
**servicePointEnabled** | **bool** | Flag indicating if delivery to service points is enabled. | [optional]
**servicePointCarriers** | **string[]** | List of carriers available for the service point picker. If service point delivery is enabled, make sure to provide at least one carrier. | [optional]
**webhookActive** | **bool** | Flag indicating if parcel updates should be sent via the webhook. | [optional]
**webhookUrl** | **string** | URL for sending updates on a parcel. A value for &#x60;webhook_url&#x60; is required if &#x60;webhook_active&#x60; is set to &#x60;true&#x60;. | [optional]
**feedbackType** | **string** | Define how your shop status feedback should be sent into your system.  Note that this will not apply to Prestashop V2 as the custom status mapping will define this.   Use the following states:    - eager: Change the parcels’ status to “sent” once the label is created.    - delayed: Change the parcels’ status to “sent” once the carrier scans the label.    - none: Don’t send any feedback. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
