# # ShippingOptionFilterParcelsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dimensions** | [**\Toppy\Sendcloud\V3\Model\StrDimensions**](StrDimensions.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\V3\Model\StrWeight**](StrWeight.md) |  | [optional]
**additionalInsuredPrice** | **float** | Amount for which you want to add additional insurance (on top of carrier insurance) to the parcel with our insurance provider XCover. You can insure up from 2 euros to 5000 euros per shipment. | [optional]
**totalInsuredPrice** | **float** | Amount for which you want to insure the parcel with (including the carrier insurance) our insurance provider XCover. If both &#x60;additional_insured_price&#x60; and &#x60;total_insured_price&#x60; are provided, &#x60;additional_insured_price&#x60; will take precedence. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
