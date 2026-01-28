# # OrdersOrderOrderDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integration** | [**\Toppy\Sendcloud\V3\Model\OrdersOrderOrderDetailsIntegration**](OrdersOrderOrderDetailsIntegration.md) |  |
**status** | [**\Toppy\Sendcloud\V3\Model\OrdersOrderOrderDetailsStatus**](OrdersOrderOrderDetailsStatus.md) |  |
**orderCreatedAt** | **\DateTime** | The date and time that the order was placed in the respective shop system in ISO 8601 |
**orderUpdatedAt** | **\DateTime** | The date and time that the order was last updated in the respective shop system in ISO 8601 | [optional]
**orderItems** | [**\Toppy\Sendcloud\V3\Model\OrderItemsInner[]**](OrderItemsInner.md) | The list of items that an order contains |
**notes** | **string** | Internal notes or comments placed by consumer on the order | [optional]
**tags** | **string[]** | Tags assigned to the order | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
