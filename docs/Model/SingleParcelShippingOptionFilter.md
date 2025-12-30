# # SingleParcelShippingOptionFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromCountryCode** | **string** | Sender country code in ISO 3166-1 alpha-2 format. | [optional]
**toCountryCode** | **string** | Destination country code in ISO 3166-1 alpha-2 format. | [optional]
**functionalities** | [**\Toppy\Sendcloud\Model\CarrierShippingFunctionalities**](CarrierShippingFunctionalities.md) |  | [optional]
**carrierCode** | **string** | Carrier code. | [optional]
**contractId** | **int** | Contract id. | [optional]
**shippingProductCode** | **string** |  | [optional]
**dimensions** | [**\Toppy\Sendcloud\Model\Dimension**](Dimension.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\Model\Weight**](Weight.md) |  | [optional]
**fromPostalCode** | **string** | The postal code of the sender address. Should be provided, to make quotes as accurate as possible. | [optional]
**toPostalCode** | **string** | The postal code of the destination address. Should be provided, to make quotes as accurate as possible. | [optional]
**totalInsurance** | **float** | Total value that you want to insure the parcel for. | [optional]
**leadTime** | [**\Toppy\Sendcloud\Model\LeadTimeFilter**](LeadTimeFilter.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
