# # CreateLabelsAsyncAllOfOrders

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parcels** | [**\Toppy\Sendcloud\V3\Model\CreateLabelParcel[]**](CreateLabelParcel.md) | Represents each package in the shipment. Each carrier can have its own limit for the number of parcels per shipment, otherwise there is a default maximum of 50 parcels. If left empty, one parcel will be created from an entire order. | [optional]
**orderId** | **string** | External order ID assigned by shop system. Used to identify an order to be shipped. |
**orderNumber** | **string** | An identification of an order in a shop system (often unique). Used to identify an order to be shipped. |
**applyShippingRules** | **bool** | Apply shipping rules to this order. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
