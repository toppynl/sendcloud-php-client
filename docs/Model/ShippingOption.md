# # ShippingOption

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | Unique identifier for this Shipping option. You can use this code to announce a parcel in the Parcel API. | [optional]
**name** | **string** | Shipping option friendly name | [optional]
**carrier** | [**\Toppy\Sendcloud\V3\Model\Carrier**](Carrier.md) |  | [optional]
**product** | [**\Toppy\Sendcloud\V3\Model\ShippingProduct**](ShippingProduct.md) |  | [optional]
**functionalities** | [**\Toppy\Sendcloud\V3\Model\CarrierShippingFunctionalities**](CarrierShippingFunctionalities.md) |  | [optional]
**maxDimensions** | [**\Toppy\Sendcloud\V3\Model\Dimension**](Dimension.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\V3\Model\ShippingQuoteWeight**](ShippingQuoteWeight.md) |  | [optional]
**parcelBilledWeights** | [**\Toppy\Sendcloud\V3\Model\ParcelBilledWeights[]**](ParcelBilledWeights.md) | If &#x60;dimensions&#x60; are provided, the volumetric weight will be calculated. The billed weight will indicate which is the highest of the regular weight and the volumetric weight. | [optional]
**contract** | [**\Toppy\Sendcloud\V3\Model\Contract**](Contract.md) |  | [optional]
**requirements** | [**\Toppy\Sendcloud\V3\Model\Requirements**](Requirements.md) |  | [optional]
**chargingType** | **string** | Specifies the timing of Sendcloud&#39;s invoicing for the shipping label.  If set to &#x60;label_creation&#x60;, the label is invoiced at the moment it is created.  If set to &#x60;first_scan&#x60;, the label is only invoiced when the carrier first scans the parcel.  The &#x60;first_scan&#x60; value is only supported for return shipping options. | [optional]
**quotes** | [**\Toppy\Sendcloud\V3\Model\ShippingQuote[]**](ShippingQuote.md) | List of available quotes.  Quotes will only be calculated if:    - &#x60;from_country_code&#x60; and &#x60;to_country_code&#x60; are to provided. - Direct contract prices are provided for the returned shipping options. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
