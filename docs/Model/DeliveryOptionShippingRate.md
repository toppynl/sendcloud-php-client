# # DeliveryOptionShippingRate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **string** | The calculated shipping rate price displayed to the end customer, based on the cart or order details, such as weight and value, and the configured shipping rates for the delivery method. * A value greater than &#x60;0&#x60; indicates the shipping rate based on the configured weight classes and rates * A value of &#x60;0&#x60; means free shipping applies, either because the cart value exceeds the free shipping threshold or a zero rate is explicitly configured * A &#x60;null&#x60; value means shipping rates are not configured for this delivery method |
**currency** | **string** | The currency of the shipping rate, as defined by the checkout configuration |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
