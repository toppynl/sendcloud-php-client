# # CreateCustomStatusMapping

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integrationId** | **int** | Sendcloud Integration ID. |
**mapping** | [**\Toppy\Sendcloud\V3\Model\CreateCustomStatusMappingMappingInner[]**](CreateCustomStatusMappingMappingInner.md) | Array containing available shop order statuses mapped onto Sendcloud&#39;s internal status category.   - Create or update an existing map of available shop order statuses onto Sendcloud&#39;s internal status category for the given integration.   - Make sure the mapping array contains objects of each Sendcloud&#39;s internal status categories.   - Map each of Sendcloud&#39;s internal status categories onto either &#x60;AvailableStatus.external_id&#x60; or &#x60;None&#x60;.   - Note that two &#x60;external_ids&#x60; may map to the same internal status category. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
