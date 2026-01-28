# # CreateLabelsBase

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integrationId** | **int** | The ID of the integration your orders belong to. |
**senderAddressId** | **int** | The ID of the sender address you would like to ship from. If not specified, your default sender address will be used.  A sender address can be added through the [Sendcloud platform](https://app.sendcloud.com/v2/settings/addresses/sender) and be retrieved using the [Retrieve a list of sender addresses](/api/v3/sender-addresses/retrieve-a-list-of-sender-addresses) endpoint. | [optional]
**brandId** | **int** | The ID of the brand. Brands can be added through the [Sendcloud platform](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved using the [Retrieve a list of brands](/api/v2/brands/retrieve-a-list-of-brands) endpoint.  &gt; **Note:** The Brands API is currently only available in API v2. This reference will be updated when a v3 version becomes available. | [optional]
**shipWith** | [**\Toppy\Sendcloud\V3\Model\ShipWith**](.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
