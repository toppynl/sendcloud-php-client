# # OrderPartialUpdateOrderDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integration** | [**\Toppy\Sendcloud\V3\Model\OrderPartialUpdateOrderDetailsIntegration**](OrderPartialUpdateOrderDetailsIntegration.md) |  | [optional]
**status** | [**\Toppy\Sendcloud\V3\Model\OrderPartialUpdateOrderDetailsStatus**](OrderPartialUpdateOrderDetailsStatus.md) |  | [optional]
**orderCreatedAt** | **\DateTime** | The date and time that the order was placed in the respective shop system in ISO 8601 | [optional]
**orderUpdatedAt** | **\DateTime** | The date and time that the order was last updated in the respective shop system in ISO 8601 | [optional]
**orderItems** | [**\Toppy\Sendcloud\V3\Model\OrderPartialUpdateOrderDetailsOrderItemsInner[]**](OrderPartialUpdateOrderDetailsOrderItemsInner.md) | List of items the order contains | [optional]
**notes** | **string** | Internal notes or comments placed by consumer on the order | [optional]
**tags** | **string[]** | Tags assigned to the order | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
