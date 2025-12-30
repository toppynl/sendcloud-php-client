# # ShippingOptionCodeProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shippingOptionCode** | **string** | The shipping option that will be or is used for shipping your parcel. A shipping option &#x60;code&#x60; can be retrieved via the [**Create a list of shipping options**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/shipping-options/operations/create-a-shipping-option) endpoint. | [optional]
**contractId** | **int** | Selected shipping contract. If you haven&#39;t specified a contract for shipping your parcel, we will automatically select the default contract for the carrier that matches your shipping option. You can retrieve your contract IDs by using the [**Retrieve a list of contracts**](https://api.sendcloud.dev/docs/sendcloud-public-api/branches/v3/contracts/operations/list-contracts) operation. Otherwise, the default direct contract will be automatically selected. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
