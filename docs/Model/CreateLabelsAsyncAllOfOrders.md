# # CreateLabelsAsyncAllOfOrders

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parcels** | [**\Toppy\Sendcloud\Model\CreateLabelParcel[]**](CreateLabelParcel.md) | Represent each package of the shipment. Each carrier can have its own number of parcels limit per shipment, otherwise there is a restriction to a maximum of 50 parcels (default). If left empty one parcel will be created from an entire order. | [optional]
**orderId** | **string** | External order ID assigned by shop system. Used to identify an order to be shipped. |
**orderNumber** | **string** | An identification of an order in a shop system (often unique). Used to identify an order to be shipped. |
**applyShippingRules** | **bool** | Apply shipping rules for this order. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
