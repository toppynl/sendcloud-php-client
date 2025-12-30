# # LabelDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mimeType** | **string** | The format of the label | [optional] [default to 'application/pdf']
**dpi** | **int** | The resolution of the label in **dots per inch**. ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities. | [optional] [default to self::DPI_NUMBER_72]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
