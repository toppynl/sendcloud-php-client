# # ShipmentRequestWithRules

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brandId** | **int** | The &#x60;id&#x60; of the brand. Brands can be added through the [Sendcloud platform](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved (alongside their &#x60;id&#x60;) from the [Retrieve a list of brands](/api/v2/brands/retrieve-a-list-of-brands) endpoint. | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](ShipWith.md) |  | [optional]
**fromAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  | [optional]
**toAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toServicePoint** | [**\Toppy\Sendcloud\Model\ServicePoint**](ServicePoint.md) |  | [optional]
**orderNumber** | **string** | Order number generated manually or by shop system | [optional]
**totalOrderPrice** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**reference** | **string** | A reference that will be stored on the Shipment and returned in your responses. This is not sent to the carrier. | [optional]
**externalReferenceId** | **string** | An optional reference can be provided by the API user; if included, it must be unique across shipments of the user. Using the same reference more than once will result in a 409 HTTP status code and the associated object being returned. | [optional]
**validationMethods** | **string[]** | A list of additional address validations to apply. At present, the only supported validation service is Here, and it is used exclusively for transactional contracts. To enable this feature, contract_id must be explicitly set and must reference a transactional contract. | [optional]
**customsInformation** | [**\Toppy\Sendcloud\Model\CustomsInformationWithOptionalFields**](CustomsInformationWithOptionalFields.md) |  | [optional]
**labelDetails** | [**\Toppy\Sendcloud\Model\LabelDetails**](LabelDetails.md) |  | [optional]
**deliveryDates** | [**\Toppy\Sendcloud\Model\DeliveryDates**](DeliveryDates.md) |  | [optional]
**parcels** | [**\Toppy\Sendcloud\Model\MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner[]**](MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner.md) | Represents each package of the shipment. Each carrier can have its own number of parcels limit per shipment, otherwise there is a restriction to a maximum of 50 parcels (default). | [optional]
**applyShippingDefaults** | **bool** | When set to &#x60;true&#x60;, the \&quot;Default weight\&quot;, \&quot;Preferred shipping method\&quot; and \&quot;Default export reason\&quot; [shipping defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults) will be applied, if they were not provided by the request payload.  **Note that the request payload values and shipping rules take precedence over these defaults.** | [optional] [default to true]
**applyShippingRules** | **bool** | When set to &#x60;true&#x60;, [shipping rules](https://app.sendcloud.com/v2/shipping/rules) will be applied.  &lt;Info&gt;   **Note that rules take precedence over the values provided in the request payload and over the [shipping defaults](https://app.sendcloud.com/v2/shipping/shipping-defaults).**      For instance, if a contract is specified in one of the applicable rules for the shipment that is being requested, the contract value provided in the request payload will be ignored.      Also keep in mind that since orders created by the API do not appear in the Sendcloud platform&#39;s Incoming Orders overview, not all shipping rules can be applied. &lt;/Info&gt; | [optional] [default to true]
**deliveryIndicator** | **string** | Free text that is intended for applying the **Checkout Delivery Method** condition in shipping rules.  Learn more about [Shipping rules](/docs/shipping/shipping-rules/). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
