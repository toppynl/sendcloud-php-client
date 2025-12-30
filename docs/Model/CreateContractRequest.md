# # CreateContractRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**isActive** | **bool** |  | [optional] [default to false]
**isDefaultPerCarrier** | **bool** | Marks the contract as default for a carrier. You can have only one default direct contract per carrier. | [optional] [default to false]
**contractData** | **array<string,string>** | Fields for creating a contract. It supports dynamic key-value pairs, where keys represent field names and values are string-based data. |
**carrierCode** | **string** | The carrier code of the contract |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
