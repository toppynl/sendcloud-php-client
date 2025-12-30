# # CreateLabelsAsync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integrationId** | **int** | ID of the integration your orders belong to. |
**senderAddressId** | **int** | ID of sender address. Address can be added through the [Sendcloud Panel](https://app.sendcloud.com/v2/settings/addresses/sender) and be retrieved through the [Sender address API](https://api.sendcloud.dev/docs/sendcloud-public-api/sender-addresses/operations/get-a-user-address-sender). | [optional]
**brandId** | **int** | ID of the brand. Brands can be added through the [Sendcloud Panel](https://app.sendcloud.com/v2/settings/brands/list) and be retrieved through the [Brands API](https://api.sendcloud.dev/docs/sendcloud-public-api/brands/operations/list-brands). | [optional]
**shipWith** | [**\Toppy\Sendcloud\Model\ShipWith**](.md) |  | [optional]
**orders** | [**\Toppy\Sendcloud\Model\CreateLabelsAsyncAllOfOrders[]**](CreateLabelsAsyncAllOfOrders.md) | Array of order objects you want to create labels for |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
