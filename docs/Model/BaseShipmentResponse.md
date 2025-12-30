# # BaseShipmentResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brandId** | **int** | &#x60;id&#x60; of the brand. Brands can be added through the [Sendcloud Panel](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved (alongside their &#x60;id&#x60;) through the [Brands API](https://api.sendcloud.dev/docs/sendcloud-public-api/brands/operations/list-brands) | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](ShipWith.md) |  |
**fromAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toServicePoint** | [**\Toppy\Sendcloud\Model\ServicePoint**](ServicePoint.md) |  | [optional]
**orderNumber** | **string** | Order number generated manually or by shop system | [optional]
**totalOrderPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**reference** | **string** | A reference that will be stored on the Shipment and returned in your responses. This is not sent to Carriers. | [optional]
**externalReferenceId** | **string** | An optional reference can be provided by the API user; if included, it must be unique across shipments of the user. Using the same reference more than once will result in a 409 HTTP status code and the associated object being returned. | [optional]
**customsInformation** | [**\Toppy\Sendcloud\Model\CustomsInformation**](CustomsInformation.md) |  | [optional]
**id** | **string** | ID of the shipment (required to retrieve or cancel a specific shipment) | [optional] [readonly]
**errors** | [**\Toppy\Sendcloud\Model\ErrorObject[]**](ErrorObject.md) | This errors object will contain errors such as carrier announcement errors or validation errors. | [optional] [readonly]
**deliveryDates** | **object** |  | [optional]
**carrier** | [**\Toppy\Sendcloud\Model\BaseShipmentResponseAllOfCarrier**](BaseShipmentResponseAllOfCarrier.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
