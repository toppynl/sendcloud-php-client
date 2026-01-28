# # ScPublicV3ScpPostShippingOptionsSimple200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**\Toppy\Sendcloud\V3\Model\ShippingOption[]**](ShippingOption.md) | A list of options to ship a parcel. A shipping option is a shipping product that the carrier offers in combination with a unique set of shipping functionalities. Each shipping option will indicate the fully allowed weight range, the requirements, the contract and the billed weight (in case weight and dimensions are passed in the request) for this option. If the request doesn&#39;t pass basic details about the parcel (e.g. from_country, to_country, and weight), it&#39;s possible that the data will be null. This is to prevent sending too many results in the response. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
