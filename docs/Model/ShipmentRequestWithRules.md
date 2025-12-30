# # ShipmentRequestWithRules

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brandId** | **int** | &#x60;id&#x60; of the brand. Brands can be added through the [Sendcloud Panel](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved (alongside their &#x60;id&#x60;) through the [Brands API](https://api.sendcloud.dev/docs/sendcloud-public-api/brands/operations/list-brands) | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](ShipWith.md) |  | [optional]
**fromAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  | [optional]
**toAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toServicePoint** | [**\Toppy\Sendcloud\Model\ServicePoint**](ServicePoint.md) |  | [optional]
**orderNumber** | **string** | Order number generated manually or by shop system | [optional]
**totalOrderPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**reference** | **string** | A reference that will be stored on the Shipment and returned in your responses. This is not sent to Carriers. | [optional]
**externalReferenceId** | **string** | An optional reference can be provided by the API user; if included, it must be unique across shipments of the user. Using the same reference more than once will result in a 409 HTTP status code and the associated object being returned. | [optional]
**customsInformation** | [**\Toppy\Sendcloud\Model\CustomsInformationWithOptionalFields**](CustomsInformationWithOptionalFields.md) |  | [optional]
**labelDetails** | [**\Toppy\Sendcloud\Model\LabelDetails**](LabelDetails.md) |  | [optional]
**deliveryDates** | **object** |  | [optional]
**parcels** | [**\Toppy\Sendcloud\Model\MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner[]**](MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner.md) | Represent each package of the shipment. Each carrier can have its own number of parcels limit per shipment, otherwise there is a restriction to a maximum of 50 parcels (default). | [optional]
**applyShippingDefaults** | **bool** | When set to true, \&quot;Default weight\&quot;, \&quot;Preferred shipping method\&quot; and \&quot;Default export reason\&quot; [shipping defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults) will be applied, whenever they were not provided by the request payload.  **Note that the request payload values and shipping rules take precedence over these defaults.** | [optional] [default to true]
**applyShippingRules** | **bool** | When set to true, [shipping rules](https://app.sendcloud.com/v2/shipping/rules) will be applied.  **Note that rules take precedence over the values provided in the request payload and over the [shipping defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults). For instance, if a contract is specified in one of the applicable rules for the shipment that is being requested, the contract value provided in the request payload will be ignored. Also keep in mind that since orders are not created in IOV by this API, not all shipping rules can be applied.** | [optional] [default to true]
**deliveryIndicator** | **string** | A free text that is intended for applying the **Checkout Delivery Method** condition in shipping rules. - Learn more about the [Shipping rules](https://sendcloud.dev/docs/shipping/shipping-rules/). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
