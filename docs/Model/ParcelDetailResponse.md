# # ParcelDetailResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brandId** | **int** | ID of the brand. Brands can be added through the [Sendcloud Panel](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved (alongside their &#x60;id&#x60;) through the [Brands API](https://api.sendcloud.dev/docs/sendcloud-public-api/brands/operations/list-brands) | [optional]
**expectedDeliveryDate** | **\DateTime** | Day when the parcel will be delivered (estimate, no timestamp) | [optional]
**integrationId** | **int** | The shop integration ID to which the provided parcel belongs | [optional]
**isMailBox** | **bool** | Indicates whether this parcel will be delivered to a mail box | [optional]
**isReturn** | **bool** | Indicates if the parcel is a return | [optional]
**isToServicePoint** | **bool** | Indicates whether this parcel is delivered to a service point (e.g. a supermarket, as opposed to a home address) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
