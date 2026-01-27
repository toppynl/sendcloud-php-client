# # UpsPickupAddress

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the person associated with the address |
**companyName** | **string** | Name of the company associated with the address | [optional]
**addressLine1** | **string** | First line of the address |
**houseNumber** | **string** | House number of the address | [optional]
**addressLine2** | **string** | Additional address information, e.g. 2nd level | [optional]
**postalCode** | **string** | Zip code of the address |
**city** | **string** | City of the address |
**poBox** | **string** | Code required in case of PO Box or post locker delivery | [optional] [readonly]
**stateProvinceCode** | **string** | The character state code of the customer represented as ISO 3166-2 code | [optional]
**countryCode** | **string** | The country code of the customer represented as ISO 3166-1 alpha-2 |
**email** | **string** | Email address of the person associated with the address | [optional]
**phoneNumber** | **string** | Phone number of the contact person in the E.164 format. | [optional]
**floor** | **string** | Floor of the pickup place. | [optional]
**room** | **string** | Room of the pickup place. | [optional]
**isAlternateAddress** | **bool** | Indicates if the pickup address is a different address than that specified in a customer&#39;s profile. | [optional] [default to false]
**isResidential** | **bool** | Indicates if the pickup address is commercial or residential. | [optional] [default to false]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
