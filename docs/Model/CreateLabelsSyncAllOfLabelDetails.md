# # CreateLabelsSyncAllOfLabelDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mimeType** | **string** | The returned format of the label. | [optional] [default to 'application/pdf']
**dpi** | **int** | DPI refers to the printing resolution of your shipping labels. It&#39;s important that labels are printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes.  Refer to the following table for DPI settings per file format:  File format | Default DPI | Valid DPI ----------- | ----------- | --------- pdf         | 72          | 72 png         | 300         | 150, 300  ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities. | [optional] [default to self::DPI_NUMBER_72]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
