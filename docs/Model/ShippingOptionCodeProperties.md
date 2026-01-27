# # ShippingOptionCodeProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shippingOptionCode** | **string** | The shipping option that will be or is used for shipping your parcel. The code can be retrieved via the [Create a list of shipping options](/api/v3/shipping-options/create-a-list-of-shipping-options) endpoint. | [optional]
**contractId** | **int** | The selected shipping contract. If you haven&#39;t specified a contract for shipping your parcel, we will automatically select the default contract for the carrier that matches your shipping option. You can retrieve your contract IDs from the [Retrieve a list of contracts](/api/v3/contracts/retrieve-a-list-of-contracts) endpoint. Otherwise, the default direct contract will be automatically selected. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
