# # LabelSyncAllOfLabelDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file** | **string** | The base64 representation of the label file. | [optional]
**mimeType** | **string** | The returned format of the label. | [optional] [default to 'application/pdf']
**dpi** | **int** | DPI refers to the printing resolution of your shipping labels. It&#39;s important that labels are printed at a high enough resolution to ensure the clarity of address details and the barcode for scanning purposes. Use following amounts for appropriate result: &lt;table&gt;   &lt;thead&gt;     &lt;tr&gt;       &lt;th&gt;File format&lt;/th&gt;       &lt;th&gt;Default DPI&lt;/th&gt;       &lt;th&gt;Valid DPI&lt;/th&gt;     &lt;/tr&gt;   &lt;/thead&gt;   &lt;tbody&gt;     &lt;tr&gt;       &lt;td&gt;pdf&lt;/td&gt;       &lt;td&gt;72&lt;/td&gt;       &lt;td&gt;72&lt;/td&gt;     &lt;/tr&gt;     &lt;tr&gt;       &lt;td&gt;png&lt;/td&gt;       &lt;td&gt;300&lt;/td&gt;       &lt;td&gt;150, 300&lt;/td&gt;     &lt;/tr&gt;   &lt;/tbody&gt; &lt;/table&gt; ZPL labels are not affected by the DPI setting, as the resolution is determined by the carrier itself. Most carriers use a resolution of 203 DPI. Zebra printers need to be configured to print at the specific DPI of the label if they have higher resolution capabilities. | [optional] [default to self::DPI_NUMBER_72]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
