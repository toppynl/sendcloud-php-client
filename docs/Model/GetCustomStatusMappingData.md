# # GetCustomStatusMappingData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integrationId** | **int** | Sendcloud Integration ID. | [optional]
**mapping** | [**\Toppy\Sendcloud\V3\Model\GetCustomStatusMappingDataMappingInner[]**](GetCustomStatusMappingDataMappingInner.md) | Array containing available shop order statuses mapped onto Sendcloud&#39;s internal status category.   - The array contains an object of each of Sendcloud&#39;s internal status categories.   - Each of sendcloud&#39;s internal status categories will be mapped onto either &#x60;AvailableStatus.external_id&#x60; or &#x60;null&#x60;   - Not all &#x60;external_ids&#x60; in AvailableStatus may be mapped onto Sendcloud&#39;s internal status category.   - Two &#x60;external_ids&#x60; may map onto the same internal status category.   - An invalid mapping is a mapping that points to &#x60;external_id&#x60; that has been deleted. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
