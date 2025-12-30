# # ParcelCustomsInformation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoiceNumber** | **string** | Customs invoice number. |
**exportReason** | **string** | Indicates the purpose or reason behind exporting the items. This classification helps customs authorities determine the applicable regulations, taxes, and duties. For Returns, this field must always be set to &#x60;returned_goods&#x60;. |
**exportType** | **string** | Export type documentation serves to categorize international shipments into three primary classifications: Private exports, intended for personal use; Commercial B2C exports, directed towards individual consumers; and Commercial B2B exports, involving business-to-business transactions. These distinctions facilitate adherence to regulatory requirements and ensure the orderly movement of goods across international boundaries. | [optional] [default to 'commercial_b2c']
**invoiceDate** | **\DateTime** | The date when the commercial invoice for the goods was issued (ISO 8601). If not provided, the announcement date will be used by default. | [optional]
**discountGranted** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**freightCosts** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**insuranceCosts** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**otherCosts** | [**\Toppy\Sendcloud\Model\OptionalPrice**](OptionalPrice.md) |  | [optional]
**generalNotes** | **string** | Exporter or shipper can include any additional information or special instructions related to the goods being shipped. This section is used to provide details that may not be covered in other parts of the invoice but are relevant for customs clearance. | [optional]
**additionalDeclarationStatements** | **string[]** | List of additional declaration statements. Each statement may contain specific details about the nature of the goods being shipped, their origin, or any additional information required by customs authorities. The content of an additional declaration statement can vary based on the requirements of the importing and exporting countries, as well as the nature of the goods being transported. | [optional]
**importerOfRecord** | [**\Toppy\Sendcloud\Model\ParcelCustomsInformationImporterOfRecord**](ParcelCustomsInformationImporterOfRecord.md) |  | [optional]
**taxNumbers** | [**\Toppy\Sendcloud\Model\ParcelCustomsInformationTaxNumbers**](ParcelCustomsInformationTaxNumbers.md) |  | [optional]
**returnData** | [**\Toppy\Sendcloud\Model\ParcelCustomsInformationReturnData**](ParcelCustomsInformationReturnData.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
