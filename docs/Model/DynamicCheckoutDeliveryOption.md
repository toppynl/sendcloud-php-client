# # DynamicCheckoutDeliveryOption

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier of the delivery method that applies to the current cart or order |
**title** | **string** | The public title of the delivery method. This can be displayed to customers during checkout |
**internalTitle** | **string** | A customizable internal name of the delivery method. It can serve as an internal identifier for the delivery option or be used for any other purpose that fits your needs |
**description** | **string** | A brief description of the delivery method. This can be used to provide additional details about the delivery option to customers during checkout |
**deliveryMethodType** | **string** | The type of the delivery method that applies to the current cart or order |
**cutOffTime** | **\DateTime** | The time until which a delivery option is valid and can be selected by the end buyer. It returns the corresponding [delivery method cut-off time](https://support.sendcloud.com/hc/en-us/articles/4404548941460#6), as configured by the merchant in Dynamic Checkout. |
**checkoutIdentifier** | [**\Toppy\Sendcloud\V3\Model\DynamicCheckoutDeliveryOptionCheckoutIdentifier**](DynamicCheckoutDeliveryOptionCheckoutIdentifier.md) |  |
**shippingRate** | [**\Toppy\Sendcloud\V3\Model\DynamicCheckoutDeliveryOptionShippingRate**](DynamicCheckoutDeliveryOptionShippingRate.md) |  |
**carrier** | [**\Toppy\Sendcloud\V3\Model\DynamicCheckoutDeliveryOptionCarrier**](DynamicCheckoutDeliveryOptionCarrier.md) |  |
**deliveryDates** | [**\Toppy\Sendcloud\V3\Model\DynamicCheckoutDeliveryOptionDeliveryDatesInner[]**](DynamicCheckoutDeliveryOptionDeliveryDatesInner.md) | A list of available delivery dates that can be presented to the customer during checkout, allowing them to select when their parcel will be delivered.  Delivery dates are calculated based on: 1. Carrier delivery days 2. Configured parcel handover days in the delivery method settings 3. Configured cut-off times in the delivery method settings 4. Any holidays defined for the delivery method  The calculation of delivery dates depends on the delivery method type:  #### Nominated Day Delivery  For &#x60;nominated_day_delivery&#x60;, up to **14** delivery dates are provided, starting from the earliest available date. Customers can choose their preferred delivery date from the list of available options.  #### Same Day Delivery For &#x60;same_day_delivery&#x60;, only **one** delivery date is provided, which always corresponds to the same day the order is placed, provided that same-day delivery is possible.  #### Standard Delivery and Service Point Delivery  For &#x60;standard_delivery&#x60; and &#x60;service_point_delivery&#x60;, delivery dates are not calculated, and the field is always set to &#x60;null&#x60;.  &lt;Info&gt;   The calculated dates are timezone-aware and are based on the timezone settings of the delivery method. &lt;/Info&gt; |
**leadTimeHours** | [**\Toppy\Sendcloud\V3\Model\DynamicCheckoutDeliveryOptionLeadTimeHours**](DynamicCheckoutDeliveryOptionLeadTimeHours.md) |  |
**sustainabilityRating** | **string** | A string representing how environmentally friendly the delivery option is, with possible values being: **low**, **medium**, and **high**, based on factors such as delivery location, delivery time, and the type of delivery vehicle. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
