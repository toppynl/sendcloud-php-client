# # ShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brandId** | **int** | The &#x60;id&#x60; of the brand. Brands can be added through the [Sendcloud platform](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved (alongside their &#x60;id&#x60;) from the [Retrieve a list of brands](/api/v2/brands/retrieve-a-list-of-brands) endpoint. | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](ShipWith.md) |  |
**fromAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toServicePoint** | [**\Toppy\Sendcloud\Model\ServicePoint**](ServicePoint.md) |  | [optional]
**orderNumber** | **string** | Order number generated manually or by shop system | [optional]
**totalOrderPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**reference** | **string** | A reference that will be stored on the Shipment and returned in your responses. This is not sent to the carrier. | [optional]
**externalReferenceId** | **string** | An optional reference can be provided by the API user; if included, it must be unique across shipments of the user. Using the same reference more than once will result in a 409 HTTP status code and the associated object being returned. | [optional]
**validationMethods** | **string[]** | A list of additional address validations to apply. At present, the only supported validation service is Here, and it is used exclusively for transactional contracts. To enable this feature, contract_id must be explicitly set and must reference a transactional contract. | [optional]
**customsInformation** | [**\Toppy\Sendcloud\Model\CustomsInformation**](CustomsInformation.md) |  | [optional]
**labelDetails** | [**\Toppy\Sendcloud\Model\LabelDetails**](LabelDetails.md) |  | [optional]
**deliveryDates** | [**\Toppy\Sendcloud\Model\DeliveryDates**](DeliveryDates.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
