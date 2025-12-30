# # ShippingOptionFilter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromCountryCode** | **string** | Sender country code in ISO 3166-1 alpha-2 format. | [optional]
**toCountryCode** | **string** | Destination country code in ISO 3166-1 alpha-2 format. | [optional]
**fromPostalCode** | **string** | The postal code of the sender address. Should be provided, to make quotes as accurate as possible. | [optional]
**toPostalCode** | **string** | The postal code of the destination address. Should be provided, to make quotes as accurate as possible. | [optional]
**toServicePointId** | **int** | Service point ID as specified in the [Service Point list](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v2/service-points/operations/list-service-points). | [optional]
**parcels** | [**\Toppy\Sendcloud\Model\ShippingOptionFilterParcelsInner[]**](ShippingOptionFilterParcelsInner.md) | List of parcels in a shipment. | [optional]
**functionalities** | [**\Toppy\Sendcloud\Model\CarrierShippingFunctionalities**](CarrierShippingFunctionalities.md) |  | [optional]
**carrierCode** | **string** | Carrier code. | [optional]
**contractId** | **int** | Contract id. | [optional]
**shippingProductCode** | **string** | Shipping product code. | [optional]
**shippingOptionCode** | **string** | Specific shipping option code to use for pricing. | [optional]
**leadTime** | [**\Toppy\Sendcloud\Model\LeadTimeFilter**](LeadTimeFilter.md) |  | [optional]
**calculateQuotes** | **bool** | If &#x60;true&#x60;, the quotes will be retrieved for the provided parcels and other parameters. If &#x60;false&#x60;, the quotes will not be retrieved, and the shipping options will be returned without quotes. This is useful when you want to return shipping options with/without retrieving quotes. Default value is &#x60;false&#x60;. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
