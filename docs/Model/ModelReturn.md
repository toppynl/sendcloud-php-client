# # ModelReturn

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**toAddress** | [**\Toppy\Sendcloud\Model\AddressWithRequiredFields**](AddressWithRequiredFields.md) |  |
**shippingProduct** | [**\Toppy\Sendcloud\Model\ShippingProductsRef**](ShippingProductsRef.md) |  |
**dimensions** | [**\Toppy\Sendcloud\Model\Dimension**](Dimension.md) |  | [optional]
**weight** | [**\Toppy\Sendcloud\Model\Weight**](Weight.md) |  |
**colloCount** | **int** | The number of collos this return consists of | [optional] [default to 1]
**parcelItems** | [**\Toppy\Sendcloud\Model\ParcelItemReturnsDetails[]**](ParcelItemReturnsDetails.md) | List of items contained in this return. Required outside EU. | [optional]
**sendTrackingEmails** | **bool** | When true Sendcloud will send out the default track and trace emails | [default to false]
**brandId** | **int** | The ID of the brand this Return belongs to. | [optional]
**labelUrl** | **string** | URL to download the label. This can be &#x60;null&#x60; because it might not be announced yet. **Deprecated** in favour of the &#x60;label&#x60; field. | [optional]
**label** | [**\Toppy\Sendcloud\Model\ReturnLabel**](ReturnLabel.md) |  | [optional]
**labelCost** | [**\Toppy\Sendcloud\Model\Price**](Price.md) |  | [optional]
**insurance** | **bool** | Whether the return parcel is insured | [optional]
**trackingNumber** | **string** | This can be null because it might not be announced yet. | [optional]
**trackingUrl** | **string** | URL to track your return. This can be null because it might not be announced yet. | [optional]
**isCancellable** | **bool** | the incoming parcel of this return can be cancelled |
**statusHistory** | [**\Toppy\Sendcloud\Model\DetailedTrackingBlobStatus[]**](DetailedTrackingBlobStatus.md) | List with the timeline of your return status |
**createdAt** | **\DateTime** | Date and time of creation of this return |
**deliveredAt** | **float** | A unix timestamp indicating the delivery time of this return. **Deprecated** in favour of the &#x60;delivered_at_iso&#x60; field. | [optional]
**deliveredAtIso** | **\DateTime** | Date and time of delivery of this return | [optional]
**reason** | [**\Toppy\Sendcloud\Model\ReturnReason**](ReturnReason.md) |  | [optional]
**refund** | [**\Toppy\Sendcloud\Model\ReturnRefund**](.md) |  | [optional]
**returnFee** | [**\Toppy\Sendcloud\Model\PriceWithAnyCurrency**](.md) |  | [optional]
**orderNumber** | **string** | Order number filled by the user | [optional]
**contract** | **int** | ID of the contract used to ship this return | [optional]
**customsInvoiceNr** | **string** | Customs invoice number | [optional]
**customsShipmentType** | **int** | Customs shipment type   * &#x60;0&#x60; - Gift   * &#x60;1&#x60; - Documents   * &#x60;2&#x60; - Commercial Goods   * &#x60;3&#x60; - Commercial Sample   * &#x60;4&#x60; - Returned Goods | [optional]
**deliveryOption** | [**\Toppy\Sendcloud\Model\DeliveryOption**](DeliveryOption.md) |  | [optional]
**images** | [**\Toppy\Sendcloud\Model\ReturnImagesInner[]**](ReturnImagesInner.md) | Images uploaded when creating a return via the Return Portal | [optional]
**status** | **string** | The current status of the return | [optional]
**customsInformation** | [**\Toppy\Sendcloud\Model\ParcelCustomsInformation**](ParcelCustomsInformation.md) |  | [optional]
**errors** | [**\Toppy\Sendcloud\Model\ErrorObject[]**](ErrorObject.md) | This array will contain errors such as carrier announcement errors. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
