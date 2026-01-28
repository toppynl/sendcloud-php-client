# toppy/sendcloud-client

Complete Sendcloud API v3 specification - merged from official sendcloud.dev documentation

For more information, please visit [https://sendcloud.dev](https://sendcloud.dev).

## Installation & Usage

### Requirements

PHP 7.2 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

Your project is free to choose the http client of your choice
Please require packages that will provide http client functionality:
https://packagist.org/providers/psr/http-client-implementation
https://packagist.org/providers/php-http/async-client-implementation
https://packagist.org/providers/psr/http-factory-implementation

As an example:

```
composer require guzzlehttp/guzzle php-http/guzzle7-adapter http-interop/http-factory-guzzle
```

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/toppy/sendcloud-client/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure HTTP basic authorization: HTTPBasicAuth
$config = Toppy\Sendcloud\V3\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Toppy\Sendcloud\V3\Api\CarrierSupportContactsApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Support contact id

try {
    $apiInstance->scPublicV3DsfDeleteCarrierSupportContacts($id);
} catch (Exception $e) {
    echo 'Exception when calling CarrierSupportContactsApi->scPublicV3DsfDeleteCarrierSupportContacts: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://panel.sendcloud.sc/api/v3*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CarrierSupportContactsApi* | [**scPublicV3DsfDeleteCarrierSupportContacts**](docs/Api/CarrierSupportContactsApi.md#scpublicv3dsfdeletecarriersupportcontacts) | **DELETE** /dsf/carrier-support-contacts/{id} | Delete a carrier support contact
*CarrierSupportContactsApi* | [**scPublicV3DsfGetCarrierSupportContacts**](docs/Api/CarrierSupportContactsApi.md#scpublicv3dsfgetcarriersupportcontacts) | **GET** /dsf/carrier-support-contacts | Retrieve carrier support contacts
*CarrierSupportContactsApi* | [**scPublicV3DsfPatchCarrierSupportContacts**](docs/Api/CarrierSupportContactsApi.md#scpublicv3dsfpatchcarriersupportcontacts) | **PATCH** /dsf/carrier-support-contacts/{id} | Update a carrier support contact
*CarrierSupportContactsApi* | [**scPublicV3DsfPostCarrierSupportContacts**](docs/Api/CarrierSupportContactsApi.md#scpublicv3dsfpostcarriersupportcontacts) | **POST** /dsf/carrier-support-contacts | Create carrier support contact
*CompatShippingOptionsApi* | [**scPublicV3ScpPostCompatShippingOptions**](docs/Api/CompatShippingOptionsApi.md#scpublicv3scppostcompatshippingoptions) | **POST** /compat/shipping-options | Retrieve a list of shipping options
*ContractsApi* | [**scPublicV3ScpDeleteContract**](docs/Api/ContractsApi.md#scpublicv3scpdeletecontract) | **DELETE** /contracts/{id} | Delete a contract
*ContractsApi* | [**scPublicV3ScpGetAllContracts**](docs/Api/ContractsApi.md#scpublicv3scpgetallcontracts) | **GET** /contracts | Retrieve a list of contracts
*ContractsApi* | [**scPublicV3ScpGetAllContractsSchemas**](docs/Api/ContractsApi.md#scpublicv3scpgetallcontractsschemas) | **GET** /contracts/schemas | Retrieve a list of contract schemas
*ContractsApi* | [**scPublicV3ScpGetSpecificContract**](docs/Api/ContractsApi.md#scpublicv3scpgetspecificcontract) | **GET** /contracts/{id} | Retrieve a contract
*ContractsApi* | [**scPublicV3ScpPatchContract**](docs/Api/ContractsApi.md#scpublicv3scppatchcontract) | **PATCH** /contracts/{id} | Update a contract
*ContractsApi* | [**scPublicV3ScpPostCreateContract**](docs/Api/ContractsApi.md#scpublicv3scppostcreatecontract) | **POST** /contracts | Create a contract for a carrier
*CreateTicketApi* | [**scPublicV3DsfPostTicketsAddressChange**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketsaddresschange) | **POST** /dsf/tickets/address-change | Create a ticket for an address change
*CreateTicketApi* | [**scPublicV3DsfPostTicketsDamage**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketsdamage) | **POST** /dsf/tickets/damage | Create a ticket for a damaged parcel
*CreateTicketApi* | [**scPublicV3DsfPostTicketsDelay**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketsdelay) | **POST** /dsf/tickets/delay | Create a ticket for a delayed parcel
*CreateTicketApi* | [**scPublicV3DsfPostTicketsDeliveredButNotReceived**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketsdeliveredbutnotreceived) | **POST** /dsf/tickets/delivered-but-not-received | Create a ticket for a delivered but not received parcel
*CreateTicketApi* | [**scPublicV3DsfPostTicketsLost**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketslost) | **POST** /dsf/tickets/lost | Create a ticket for a lost parcel
*CreateTicketApi* | [**scPublicV3DsfPostTicketsUnjustReturn**](docs/Api/CreateTicketApi.md#scpublicv3dsfpostticketsunjustreturn) | **POST** /dsf/tickets/unjust-return | Create a ticket for an unjustly returned parcel
*DeliveryOptionsApi* | [**scPublicV3CheckoutApiGetDeliveryOptions**](docs/Api/DeliveryOptionsApi.md#scpublicv3checkoutapigetdeliveryoptions) | **GET** /checkout/configurations/{configuration_id}/delivery-options | Retrieve a list of delivery options
*FileUploadApi* | [**scPublicV3DsfPostFiles**](docs/Api/FileUploadApi.md#scpublicv3dsfpostfiles) | **POST** /dsf/files | Upload a file
*IntegrationsApi* | [**scPublicV3IntegrationsDeleteDeleteIntegration**](docs/Api/IntegrationsApi.md#scpublicv3integrationsdeletedeleteintegration) | **DELETE** /integrations/{id} | Delete an integration
*IntegrationsApi* | [**scPublicV3IntegrationsGetListIntegrations**](docs/Api/IntegrationsApi.md#scpublicv3integrationsgetlistintegrations) | **GET** /integrations | Retrieve a list of integrations
*IntegrationsApi* | [**scPublicV3IntegrationsGetRetrieveIntegration**](docs/Api/IntegrationsApi.md#scpublicv3integrationsgetretrieveintegration) | **GET** /integrations/{id} | Retrieve an integration
*IntegrationsApi* | [**scPublicV3IntegrationsGetShopOrderStatuses**](docs/Api/IntegrationsApi.md#scpublicv3integrationsgetshoporderstatuses) | **GET** /shop-order-statuses | Retrieve shop order statuses for an integration
*IntegrationsApi* | [**scPublicV3IntegrationsGetShopOrderStatusesMapping**](docs/Api/IntegrationsApi.md#scpublicv3integrationsgetshoporderstatusesmapping) | **GET** /shop-order-statuses/mapping | Retrieve custom status mapping for an integration
*IntegrationsApi* | [**scPublicV3IntegrationsPatchUpdateIntegration**](docs/Api/IntegrationsApi.md#scpublicv3integrationspatchupdateintegration) | **PATCH** /integrations/{id} | Update certain parts of an integration
*IntegrationsApi* | [**scPublicV3IntegrationsPostShopOrderStatuses**](docs/Api/IntegrationsApi.md#scpublicv3integrationspostshoporderstatuses) | **POST** /shop-order-statuses | Create or overwrite shop order statuses
*IntegrationsApi* | [**scPublicV3IntegrationsPostShopOrderStatusesMapping**](docs/Api/IntegrationsApi.md#scpublicv3integrationspostshoporderstatusesmapping) | **POST** /shop-order-statuses/mapping | Create or update custom status mapping for an integration
*OAuth2Api* | [**oAuth2TokenExchange**](docs/Api/OAuth2Api.md#oauth2tokenexchange) | **POST** /oauth2/token | OAuth 2.0 token
*OrdersApi* | [**scPublicV3OrdersDeleteDeleteOrder**](docs/Api/OrdersApi.md#scpublicv3ordersdeletedeleteorder) | **DELETE** /orders/{id} | Delete an order
*OrdersApi* | [**scPublicV3OrdersGetListOrders**](docs/Api/OrdersApi.md#scpublicv3ordersgetlistorders) | **GET** /orders | Retrieve a list of orders
*OrdersApi* | [**scPublicV3OrdersGetRetrieveOrder**](docs/Api/OrdersApi.md#scpublicv3ordersgetretrieveorder) | **GET** /orders/{id} | Retrieve an order
*OrdersApi* | [**scPublicV3OrdersPatchPartialUpdateOrder**](docs/Api/OrdersApi.md#scpublicv3orderspatchpartialupdateorder) | **PATCH** /orders/{id} | Update an order
*OrdersApi* | [**scPublicV3OrdersPostCreateOrders**](docs/Api/OrdersApi.md#scpublicv3orderspostcreateorders) | **POST** /orders | Create/Update orders in batch
*ParcelDocumentsApi* | [**scPublicV3ScpGetRetrieveParcelDocuments**](docs/Api/ParcelDocumentsApi.md#scpublicv3scpgetretrieveparceldocuments) | **GET** /parcels/{id}/documents/{type} | Retrieve a parcel document
*ParcelDocumentsApi* | [**scPublicV3ScpGetRetrieveParcelDocumentsBulk**](docs/Api/ParcelDocumentsApi.md#scpublicv3scpgetretrieveparceldocumentsbulk) | **GET** /parcel-documents/{type} | Retrieve multiple parcel documents
*ParcelStatusesApi* | [**scPublicV3ScpGetAllParcelStatuses**](docs/Api/ParcelStatusesApi.md#scpublicv3scpgetallparcelstatuses) | **GET** /parcels/statuses | Retrieve a list of parcel statuses
*ParcelTrackingApi* | [**scPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber**](docs/Api/ParcelTrackingApi.md#scpublicv3shippingintelligenceenginegetgetparcelbytrackingnumber) | **GET** /parcels/tracking/{tracking_number} | Retrieve tracking information for a parcel
*ParcelTrackingApi* | [**scPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking**](docs/Api/ParcelTrackingApi.md#scpublicv3shippingintelligenceenginepostregisterparcelfortracking) | **POST** /parcels/tracking | Create a tracking-only parcel
*PickupsApi* | [**scPublicV3ScpGetAllPickups**](docs/Api/PickupsApi.md#scpublicv3scpgetallpickups) | **GET** /pickups | Retrieve a list of pickups
*PickupsApi* | [**scPublicV3ScpGetPickup**](docs/Api/PickupsApi.md#scpublicv3scpgetpickup) | **GET** /pickups/{id} | Retrieve a pickup
*PickupsApi* | [**scPublicV3ScpPostPickup**](docs/Api/PickupsApi.md#scpublicv3scppostpickup) | **POST** /pickups | Create a pickup
*RequestedDataApi* | [**scPublicV3DsfGetRequestedData**](docs/Api/RequestedDataApi.md#scpublicv3dsfgetrequesteddata) | **GET** /support/dsf/tickets/requested-data | Retrieve requested data for open tickets
*RequestedDataApi* | [**scPublicV3DsfPostRequestedData**](docs/Api/RequestedDataApi.md#scpublicv3dsfpostrequesteddata) | **POST** /support/dsf/tickets/requested-data | Provide requested data
*ReturnsApi* | [**scPublicV3ScpGetReturnsGetDetails**](docs/Api/ReturnsApi.md#scpublicv3scpgetreturnsgetdetails) | **GET** /returns/{id} | Retrieve a return
*ReturnsApi* | [**scPublicV3ScpGetReturnsGetReturns**](docs/Api/ReturnsApi.md#scpublicv3scpgetreturnsgetreturns) | **GET** /returns | Retrieve a list of returns
*ReturnsApi* | [**scPublicV3ScpPatchReturnsCancel**](docs/Api/ReturnsApi.md#scpublicv3scppatchreturnscancel) | **PATCH** /returns/{id}/cancel | Request cancellation of a return
*ReturnsApi* | [**scPublicV3ScpPostReturnsCreateNewReturn**](docs/Api/ReturnsApi.md#scpublicv3scppostreturnscreatenewreturn) | **POST** /returns | Create a return
*ReturnsApi* | [**scPublicV3ScpPostReturnsCreateNewReturnSynchronously**](docs/Api/ReturnsApi.md#scpublicv3scppostreturnscreatenewreturnsynchronously) | **POST** /returns/announce-synchronously | Create a return synchronously
*ReturnsApi* | [**scPublicV3ScpPostReturnsValidate**](docs/Api/ReturnsApi.md#scpublicv3scppostreturnsvalidate) | **POST** /returns/validate | Validate a return
*SenderAddressApi* | [**scPublicV3AddressesGetAllSenderAddresses**](docs/Api/SenderAddressApi.md#scpublicv3addressesgetallsenderaddresses) | **GET** /addresses/sender-addresses | Retrieve a list of sender addresses
*SenderAddressApi* | [**scPublicV3AddressesGetSenderAddressById**](docs/Api/SenderAddressApi.md#scpublicv3addressesgetsenderaddressbyid) | **GET** /addresses/sender-addresses/{id} | Retrieve a sender address
*ShipAnOrderApi* | [**scPublicV3OrdersLabelsPostCreateLabelsAsync**](docs/Api/ShipAnOrderApi.md#scpublicv3orderslabelspostcreatelabelsasync) | **POST** /orders/create-labels-async | Request a label for one or more orders asynchronously
*ShipAnOrderApi* | [**scPublicV3OrdersLabelsPostCreateLabelsSync**](docs/Api/ShipAnOrderApi.md#scpublicv3orderslabelspostcreatelabelssync) | **POST** /orders/create-label-sync | Request a label for a single order synchronously
*ShipmentsApi* | [**scPublicV3ScpGetAllShipments**](docs/Api/ShipmentsApi.md#scpublicv3scpgetallshipments) | **GET** /shipments | Retrieve shipments
*ShipmentsApi* | [**scPublicV3ScpGetShipmentById**](docs/Api/ShipmentsApi.md#scpublicv3scpgetshipmentbyid) | **GET** /shipments/{id} | Retrieve a shipment
*ShipmentsApi* | [**scPublicV3ScpPostAnnounceShipment**](docs/Api/ShipmentsApi.md#scpublicv3scppostannounceshipment) | **POST** /shipments/announce | Create and announce a shipment synchronously
*ShipmentsApi* | [**scPublicV3ScpPostAnnounceShipmentWithRules**](docs/Api/ShipmentsApi.md#scpublicv3scppostannounceshipmentwithrules) | **POST** /shipments/announce-with-shipping-rules | Create a shipment with rules and/or defaults and announce it synchronously
*ShipmentsApi* | [**scPublicV3ScpPostCancelShipment**](docs/Api/ShipmentsApi.md#scpublicv3scppostcancelshipment) | **POST** /shipments/{id}/cancel | Cancel a shipment
*ShipmentsApi* | [**scPublicV3ScpPostCreateShipment**](docs/Api/ShipmentsApi.md#scpublicv3scppostcreateshipment) | **POST** /shipments | Create and announce a shipment asynchronously
*ShipmentsApi* | [**scPublicV3ScpPostCreateShipmentWithRules**](docs/Api/ShipmentsApi.md#scpublicv3scppostcreateshipmentwithrules) | **POST** /shipments/create-with-shipping-rules | Create a shipment with rules and/or defaults and announce it asynchronously
*ShippingOptionsApi* | [**scPublicV3ScpPostShippingOptions**](docs/Api/ShippingOptionsApi.md#scpublicv3scppostshippingoptions) | **POST** /shipping-options | Return a list of available shipping options
*ShippingOptionsApi* | [**scPublicV3ScpPostShippingOptionsSimple**](docs/Api/ShippingOptionsApi.md#scpublicv3scppostshippingoptionssimple) | **POST** /fetch-shipping-options | Create a list of shipping options
*UserApi* | [**scPublicV3ScpGetUserAuthMetadata**](docs/Api/UserApi.md#scpublicv3scpgetuserauthmetadata) | **GET** /user/auth/metadata | Retrieve metadata associated with the authentication method

## Models

- [Address](docs/Model/Address.md)
- [AddressWithRequiredFields](docs/Model/AddressWithRequiredFields.md)
- [AnnouncedShipmentIncludingLabel](docs/Model/AnnouncedShipmentIncludingLabel.md)
- [BaseContractFieldSchema](docs/Model/BaseContractFieldSchema.md)
- [BaseContractFieldSchemaChoicesInner](docs/Model/BaseContractFieldSchemaChoicesInner.md)
- [BaseContractRequest](docs/Model/BaseContractRequest.md)
- [BasePickupItem](docs/Model/BasePickupItem.md)
- [BasePickupRequest](docs/Model/BasePickupRequest.md)
- [BasePickupResponse](docs/Model/BasePickupResponse.md)
- [BaseShipmentResponse](docs/Model/BaseShipmentResponse.md)
- [BilledWeightType](docs/Model/BilledWeightType.md)
- [BrtPickupRequest](docs/Model/BrtPickupRequest.md)
- [BrtPickupResponse](docs/Model/BrtPickupResponse.md)
- [CancelShipmentStatus](docs/Model/CancelShipmentStatus.md)
- [CancellationStatus](docs/Model/CancellationStatus.md)
- [Carrier](docs/Model/Carrier.md)
- [CarrierClaimForm](docs/Model/CarrierClaimForm.md)
- [CarrierCodeField](docs/Model/CarrierCodeField.md)
- [CarrierLanguageField](docs/Model/CarrierLanguageField.md)
- [CarrierShippingFunctionalities](docs/Model/CarrierShippingFunctionalities.md)
- [CarrierSpecificData](docs/Model/CarrierSpecificData.md)
- [CarrierSupportContact](docs/Model/CarrierSupportContact.md)
- [CompatShippingOptionsResponse](docs/Model/CompatShippingOptionsResponse.md)
- [ContentsPurchaseValueField](docs/Model/ContentsPurchaseValueField.md)
- [ContentsSalesValueField](docs/Model/ContentsSalesValueField.md)
- [Contract](docs/Model/Contract.md)
- [ContractCreatedResponse](docs/Model/ContractCreatedResponse.md)
- [ContractProperties](docs/Model/ContractProperties.md)
- [ContractSchema](docs/Model/ContractSchema.md)
- [ContractSchemaFieldsInner](docs/Model/ContractSchemaFieldsInner.md)
- [CorreosExpressPickupRequest](docs/Model/CorreosExpressPickupRequest.md)
- [CorreosExpressPickupResponse](docs/Model/CorreosExpressPickupResponse.md)
- [CorreosPickupItem](docs/Model/CorreosPickupItem.md)
- [CorreosPickupRequest](docs/Model/CorreosPickupRequest.md)
- [CorreosPickupResponse](docs/Model/CorreosPickupResponse.md)
- [CostsObject](docs/Model/CostsObject.md)
- [CreateAddressChangeOwnContract](docs/Model/CreateAddressChangeOwnContract.md)
- [CreateAddressChangeTransactional](docs/Model/CreateAddressChangeTransactional.md)
- [CreateContractRequest](docs/Model/CreateContractRequest.md)
- [CreateCustomStatusMapping](docs/Model/CreateCustomStatusMapping.md)
- [CreateCustomStatusMappingMappingInner](docs/Model/CreateCustomStatusMappingMappingInner.md)
- [CreateDamagedOwnContract](docs/Model/CreateDamagedOwnContract.md)
- [CreateDamagedTransactional](docs/Model/CreateDamagedTransactional.md)
- [CreateDelayedOwnContract](docs/Model/CreateDelayedOwnContract.md)
- [CreateDelayedTransactional](docs/Model/CreateDelayedTransactional.md)
- [CreateDeliveredButNotReceivedOwnContract](docs/Model/CreateDeliveredButNotReceivedOwnContract.md)
- [CreateDeliveredButNotReceivedTransactional](docs/Model/CreateDeliveredButNotReceivedTransactional.md)
- [CreateLabelParcel](docs/Model/CreateLabelParcel.md)
- [CreateLabelsAsync](docs/Model/CreateLabelsAsync.md)
- [CreateLabelsAsyncAllOfOrders](docs/Model/CreateLabelsAsyncAllOfOrders.md)
- [CreateLabelsBase](docs/Model/CreateLabelsBase.md)
- [CreateLabelsParcels](docs/Model/CreateLabelsParcels.md)
- [CreateLabelsSync](docs/Model/CreateLabelsSync.md)
- [CreateLabelsSyncAllOfLabelDetails](docs/Model/CreateLabelsSyncAllOfLabelDetails.md)
- [CreateLostOwnContract](docs/Model/CreateLostOwnContract.md)
- [CreateLostTransactional](docs/Model/CreateLostTransactional.md)
- [CreateSupportContactRequest](docs/Model/CreateSupportContactRequest.md)
- [CreateTicketResponseSchema](docs/Model/CreateTicketResponseSchema.md)
- [CreateUnjustReturnOwnContract](docs/Model/CreateUnjustReturnOwnContract.md)
- [CreateUnjustReturnTransactional](docs/Model/CreateUnjustReturnTransactional.md)
- [CurrencyType](docs/Model/CurrencyType.md)
- [CustomerConfirmationField](docs/Model/CustomerConfirmationField.md)
- [CustomerDetails](docs/Model/CustomerDetails.md)
- [CustomsDetails](docs/Model/CustomsDetails.md)
- [CustomsInformation](docs/Model/CustomsInformation.md)
- [CustomsInformationWithOptionalFields](docs/Model/CustomsInformationWithOptionalFields.md)
- [DamagePhoto1Field](docs/Model/DamagePhoto1Field.md)
- [DamagePhoto2Field](docs/Model/DamagePhoto2Field.md)
- [DangerousGoods](docs/Model/DangerousGoods.md)
- [DeliveryDates](docs/Model/DeliveryDates.md)
- [DeliveryOption](docs/Model/DeliveryOption.md)
- [DeliveryOptionCarrier](docs/Model/DeliveryOptionCarrier.md)
- [DeliveryOptionCheckoutIdentifier](docs/Model/DeliveryOptionCheckoutIdentifier.md)
- [DeliveryOptionDeliveryDatesInner](docs/Model/DeliveryOptionDeliveryDatesInner.md)
- [DeliveryOptionLeadTimeHours](docs/Model/DeliveryOptionLeadTimeHours.md)
- [DeliveryOptionShippingRate](docs/Model/DeliveryOptionShippingRate.md)
- [DeliveryOptionsResponse](docs/Model/DeliveryOptionsResponse.md)
- [DetailedTrackingBlobStatus](docs/Model/DetailedTrackingBlobStatus.md)
- [DhlDePickupItem](docs/Model/DhlDePickupItem.md)
- [DhlDePickupRequest](docs/Model/DhlDePickupRequest.md)
- [DhlDePickupResponse](docs/Model/DhlDePickupResponse.md)
- [DhlDeReturnsObject](docs/Model/DhlDeReturnsObject.md)
- [DhlExpressPickupRequest](docs/Model/DhlExpressPickupRequest.md)
- [DhlExpressPickupResponse](docs/Model/DhlExpressPickupResponse.md)
- [DhlParcelGbPickupRequest](docs/Model/DhlParcelGbPickupRequest.md)
- [DhlParcelGbPickupResponse](docs/Model/DhlParcelGbPickupResponse.md)
- [DhlParcelIberiaPickupRequest](docs/Model/DhlParcelIberiaPickupRequest.md)
- [DhlParcelIberiaPickupResponse](docs/Model/DhlParcelIberiaPickupResponse.md)
- [DhlPickupItem](docs/Model/DhlPickupItem.md)
- [DhlPickupRequest](docs/Model/DhlPickupRequest.md)
- [DhlPickupResponse](docs/Model/DhlPickupResponse.md)
- [Dimension](docs/Model/Dimension.md)
- [DimensionUnit](docs/Model/DimensionUnit.md)
- [DimensionUnits](docs/Model/DimensionUnits.md)
- [Documents](docs/Model/Documents.md)
- [DpdAtPickupItem](docs/Model/DpdAtPickupItem.md)
- [DpdAtPickupRequest](docs/Model/DpdAtPickupRequest.md)
- [DpdAtPickupResponse](docs/Model/DpdAtPickupResponse.md)
- [DpdPickupRequest](docs/Model/DpdPickupRequest.md)
- [DpdPickupResponse](docs/Model/DpdPickupResponse.md)
- [EntireProductPhotoField](docs/Model/EntireProductPhotoField.md)
- [ErrorOAuth2](docs/Model/ErrorOAuth2.md)
- [ErrorObject](docs/Model/ErrorObject.md)
- [ErrorObjectLinks](docs/Model/ErrorObjectLinks.md)
- [ErrorObjectSource](docs/Model/ErrorObjectSource.md)
- [Errors](docs/Model/Errors.md)
- [ErrorsResponseSchema](docs/Model/ErrorsResponseSchema.md)
- [ErrorsResponseSchemaErrorsInner](docs/Model/ErrorsResponseSchemaErrorsInner.md)
- [ExteriorPhotoField](docs/Model/ExteriorPhotoField.md)
- [FedexOriginDetail](docs/Model/FedexOriginDetail.md)
- [FedexRequest](docs/Model/FedexRequest.md)
- [FedexResponse](docs/Model/FedexResponse.md)
- [GetCustomStatusMapping](docs/Model/GetCustomStatusMapping.md)
- [GetCustomStatusMappingData](docs/Model/GetCustomStatusMappingData.md)
- [GetCustomStatusMappingDataMappingInner](docs/Model/GetCustomStatusMappingDataMappingInner.md)
- [GetShopOrderStatuses](docs/Model/GetShopOrderStatuses.md)
- [GetShopOrderStatusesDataInner](docs/Model/GetShopOrderStatusesDataInner.md)
- [GetShopOrderStatusesDataInnerTranslationsInner](docs/Model/GetShopOrderStatusesDataInnerTranslationsInner.md)
- [GlsItRequest](docs/Model/GlsItRequest.md)
- [GlsItResponse](docs/Model/GlsItResponse.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [HermesDePickupRequest](docs/Model/HermesDePickupRequest.md)
- [HermesDePickupResponse](docs/Model/HermesDePickupResponse.md)
- [IdentificationNumbersAndCodesRelatedToSenderReceiverAndImporterOfRecordProvider](docs/Model/IdentificationNumbersAndCodesRelatedToSenderReceiverAndImporterOfRecordProvider.md)
- [Insurance](docs/Model/Insurance.md)
- [IntegrationGetResponse](docs/Model/IntegrationGetResponse.md)
- [IntegrationListResponse](docs/Model/IntegrationListResponse.md)
- [IntegrationModel](docs/Model/IntegrationModel.md)
- [IntegrationResponseModel](docs/Model/IntegrationResponseModel.md)
- [InteriorPhotoField](docs/Model/InteriorPhotoField.md)
- [LabelAsync](docs/Model/LabelAsync.md)
- [LabelBase](docs/Model/LabelBase.md)
- [LabelDetails](docs/Model/LabelDetails.md)
- [LabelSync](docs/Model/LabelSync.md)
- [LabelSyncAllOfLabelDetails](docs/Model/LabelSyncAllOfLabelDetails.md)
- [LeadTimeFilter](docs/Model/LeadTimeFilter.md)
- [ListPickupResponse](docs/Model/ListPickupResponse.md)
- [LocationInner](docs/Model/LocationInner.md)
- [Measurement](docs/Model/Measurement.md)
- [MeasurementPartialUpdate](docs/Model/MeasurementPartialUpdate.md)
- [MeasurementPartialUpdateDimension](docs/Model/MeasurementPartialUpdateDimension.md)
- [MeasurementPartialUpdateVolume](docs/Model/MeasurementPartialUpdateVolume.md)
- [MeasurementPartialUpdateWeight](docs/Model/MeasurementPartialUpdateWeight.md)
- [ModelReturn](docs/Model/ModelReturn.md)
- [MulticolloParcelsArrayRequest](docs/Model/MulticolloParcelsArrayRequest.md)
- [MulticolloParcelsArrayRequestWithOptionalFields](docs/Model/MulticolloParcelsArrayRequestWithOptionalFields.md)
- [MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner](docs/Model/MulticolloParcelsArrayRequestWithOptionalFieldsParcelsInner.md)
- [OAuth2TokenExchange](docs/Model/OAuth2TokenExchange.md)
- [OptionalPrice](docs/Model/OptionalPrice.md)
- [Order](docs/Model/Order.md)
- [OrderCreateRequest](docs/Model/OrderCreateRequest.md)
- [OrderItem](docs/Model/OrderItem.md)
- [OrderItemsInner](docs/Model/OrderItemsInner.md)
- [OrderOrderDetails](docs/Model/OrderOrderDetails.md)
- [OrderOrderDetailsIntegration](docs/Model/OrderOrderDetailsIntegration.md)
- [OrderOrderDetailsStatus](docs/Model/OrderOrderDetailsStatus.md)
- [OrderPartialUpdate](docs/Model/OrderPartialUpdate.md)
- [OrderPartialUpdateCustomerDetails](docs/Model/OrderPartialUpdateCustomerDetails.md)
- [OrderPartialUpdateOrderDetails](docs/Model/OrderPartialUpdateOrderDetails.md)
- [OrderPartialUpdateOrderDetailsIntegration](docs/Model/OrderPartialUpdateOrderDetailsIntegration.md)
- [OrderPartialUpdateOrderDetailsOrderItemsInner](docs/Model/OrderPartialUpdateOrderDetailsOrderItemsInner.md)
- [OrderPartialUpdateOrderDetailsOrderItemsInnerDeliveryDates](docs/Model/OrderPartialUpdateOrderDetailsOrderItemsInnerDeliveryDates.md)
- [OrderPartialUpdateOrderDetailsStatus](docs/Model/OrderPartialUpdateOrderDetailsStatus.md)
- [OrderPartialUpdatePaymentDetails](docs/Model/OrderPartialUpdatePaymentDetails.md)
- [OrderPartialUpdatePaymentDetailsStatus](docs/Model/OrderPartialUpdatePaymentDetailsStatus.md)
- [OrderPartialUpdateServicePointDetails](docs/Model/OrderPartialUpdateServicePointDetails.md)
- [OrderPartialUpdateShippingDetails](docs/Model/OrderPartialUpdateShippingDetails.md)
- [OrderSelectorOrderIdRequired](docs/Model/OrderSelectorOrderIdRequired.md)
- [OrderSelectorOrderNumberRequired](docs/Model/OrderSelectorOrderNumberRequired.md)
- [PackagePhotoField](docs/Model/PackagePhotoField.md)
- [ParcelBilledWeights](docs/Model/ParcelBilledWeights.md)
- [ParcelCommon](docs/Model/ParcelCommon.md)
- [ParcelCommonWithOptionalFields](docs/Model/ParcelCommonWithOptionalFields.md)
- [ParcelCustomsInformation](docs/Model/ParcelCustomsInformation.md)
- [ParcelCustomsInformationImporterOfRecord](docs/Model/ParcelCustomsInformationImporterOfRecord.md)
- [ParcelCustomsInformationReturnData](docs/Model/ParcelCustomsInformationReturnData.md)
- [ParcelCustomsInformationTaxNumbers](docs/Model/ParcelCustomsInformationTaxNumbers.md)
- [ParcelDetailCreateRequest](docs/Model/ParcelDetailCreateRequest.md)
- [ParcelDetailResponse](docs/Model/ParcelDetailResponse.md)
- [ParcelDimensionsField](docs/Model/ParcelDimensionsField.md)
- [ParcelEventResponse](docs/Model/ParcelEventResponse.md)
- [ParcelItem](docs/Model/ParcelItem.md)
- [ParcelItemReturnsCreate](docs/Model/ParcelItemReturnsCreate.md)
- [ParcelItemReturnsDetails](docs/Model/ParcelItemReturnsDetails.md)
- [ParcelItemWithOptionalFields](docs/Model/ParcelItemWithOptionalFields.md)
- [ParcelItemWithSourceId](docs/Model/ParcelItemWithSourceId.md)
- [ParcelStatus](docs/Model/ParcelStatus.md)
- [ParcelTrackingAddress](docs/Model/ParcelTrackingAddress.md)
- [ParcelTrackingCreateRequest](docs/Model/ParcelTrackingCreateRequest.md)
- [ParcelTrackingCreateResponse](docs/Model/ParcelTrackingCreateResponse.md)
- [ParcelTrackingResponse](docs/Model/ParcelTrackingResponse.md)
- [ParcelsArrayResponse](docs/Model/ParcelsArrayResponse.md)
- [PatchSupportContactRequest](docs/Model/PatchSupportContactRequest.md)
- [PaymentDetails](docs/Model/PaymentDetails.md)
- [PaymentDetailsStatus](docs/Model/PaymentDetailsStatus.md)
- [PickupAddress](docs/Model/PickupAddress.md)
- [PickupAddressPhoneNumberRequired](docs/Model/PickupAddressPhoneNumberRequired.md)
- [PickupAddressStateProvinceRequired](docs/Model/PickupAddressStateProvinceRequired.md)
- [PostShopOrderStatuses](docs/Model/PostShopOrderStatuses.md)
- [PostShopOrderStatusesStatusesInner](docs/Model/PostShopOrderStatusesStatusesInner.md)
- [PostShopOrderStatusesStatusesInnerTranslationsInner](docs/Model/PostShopOrderStatusesStatusesInnerTranslationsInner.md)
- [PosteItDeliveryPickupRequest](docs/Model/PosteItDeliveryPickupRequest.md)
- [PosteItDeliveryPickupResponse](docs/Model/PosteItDeliveryPickupResponse.md)
- [Price](docs/Model/Price.md)
- [PriceWithAnyCurrency](docs/Model/PriceWithAnyCurrency.md)
- [PurchaseInvoiceField](docs/Model/PurchaseInvoiceField.md)
- [RequiredPrice](docs/Model/RequiredPrice.md)
- [Requirements](docs/Model/Requirements.md)
- [ReturnImagesInner](docs/Model/ReturnImagesInner.md)
- [ReturnLabel](docs/Model/ReturnLabel.md)
- [ReturnReason](docs/Model/ReturnReason.md)
- [ReturnRefund](docs/Model/ReturnRefund.md)
- [ReturnValidation](docs/Model/ReturnValidation.md)
- [ReturnValidationDimensions](docs/Model/ReturnValidationDimensions.md)
- [SalesInvoiceField](docs/Model/SalesInvoiceField.md)
- [ScPublicV3AddressesGetAllSenderAddresses200Response](docs/Model/ScPublicV3AddressesGetAllSenderAddresses200Response.md)
- [ScPublicV3AddressesGetSenderAddressById200Response](docs/Model/ScPublicV3AddressesGetSenderAddressById200Response.md)
- [ScPublicV3DsfGetRequestedData200Response](docs/Model/ScPublicV3DsfGetRequestedData200Response.md)
- [ScPublicV3DsfGetRequestedData200ResponseDataInner](docs/Model/ScPublicV3DsfGetRequestedData200ResponseDataInner.md)
- [ScPublicV3DsfPostFiles201Response](docs/Model/ScPublicV3DsfPostFiles201Response.md)
- [ScPublicV3DsfPostRequestedDataRequest](docs/Model/ScPublicV3DsfPostRequestedDataRequest.md)
- [ScPublicV3DsfPostRequestedDataRequestAttachmentsInner](docs/Model/ScPublicV3DsfPostRequestedDataRequestAttachmentsInner.md)
- [ScPublicV3DsfPostRequestedDataRequestSalesDataInner](docs/Model/ScPublicV3DsfPostRequestedDataRequestSalesDataInner.md)
- [ScPublicV3DsfPostTicketsAddressChangeRequest](docs/Model/ScPublicV3DsfPostTicketsAddressChangeRequest.md)
- [ScPublicV3DsfPostTicketsDamageRequest](docs/Model/ScPublicV3DsfPostTicketsDamageRequest.md)
- [ScPublicV3DsfPostTicketsDelayRequest](docs/Model/ScPublicV3DsfPostTicketsDelayRequest.md)
- [ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest](docs/Model/ScPublicV3DsfPostTicketsDeliveredButNotReceivedRequest.md)
- [ScPublicV3DsfPostTicketsLostRequest](docs/Model/ScPublicV3DsfPostTicketsLostRequest.md)
- [ScPublicV3DsfPostTicketsUnjustReturnRequest](docs/Model/ScPublicV3DsfPostTicketsUnjustReturnRequest.md)
- [ScPublicV3OrdersGetListOrders200Response](docs/Model/ScPublicV3OrdersGetListOrders200Response.md)
- [ScPublicV3OrdersGetRetrieveOrder200Response](docs/Model/ScPublicV3OrdersGetRetrieveOrder200Response.md)
- [ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response](docs/Model/ScPublicV3OrdersLabelsPostCreateLabelsAsync202Response.md)
- [ScPublicV3OrdersLabelsPostCreateLabelsSync201Response](docs/Model/ScPublicV3OrdersLabelsPostCreateLabelsSync201Response.md)
- [ScPublicV3OrdersPatchPartialUpdateOrder200Response](docs/Model/ScPublicV3OrdersPatchPartialUpdateOrder200Response.md)
- [ScPublicV3OrdersPatchPartialUpdateOrder200ResponseData](docs/Model/ScPublicV3OrdersPatchPartialUpdateOrder200ResponseData.md)
- [ScPublicV3OrdersPostCreateOrders201Response](docs/Model/ScPublicV3OrdersPostCreateOrders201Response.md)
- [ScPublicV3OrdersPostCreateOrders201ResponseDataInner](docs/Model/ScPublicV3OrdersPostCreateOrders201ResponseDataInner.md)
- [ScPublicV3OrdersPostCreateOrdersRequestInner](docs/Model/ScPublicV3OrdersPostCreateOrdersRequestInner.md)
- [ScPublicV3ScpGetAllContracts200Response](docs/Model/ScPublicV3ScpGetAllContracts200Response.md)
- [ScPublicV3ScpGetAllContractsSchemas200Response](docs/Model/ScPublicV3ScpGetAllContractsSchemas200Response.md)
- [ScPublicV3ScpGetAllParcelStatuses200Response](docs/Model/ScPublicV3ScpGetAllParcelStatuses200Response.md)
- [ScPublicV3ScpGetAllPickups200Response](docs/Model/ScPublicV3ScpGetAllPickups200Response.md)
- [ScPublicV3ScpGetAllShipments200Response](docs/Model/ScPublicV3ScpGetAllShipments200Response.md)
- [ScPublicV3ScpGetAllShipmentsParcelStatusParameter](docs/Model/ScPublicV3ScpGetAllShipmentsParcelStatusParameter.md)
- [ScPublicV3ScpGetPickup200Response](docs/Model/ScPublicV3ScpGetPickup200Response.md)
- [ScPublicV3ScpGetPickup200ResponseData](docs/Model/ScPublicV3ScpGetPickup200ResponseData.md)
- [ScPublicV3ScpGetReturnsGetReturns200Response](docs/Model/ScPublicV3ScpGetReturnsGetReturns200Response.md)
- [ScPublicV3ScpGetShipmentById200Response](docs/Model/ScPublicV3ScpGetShipmentById200Response.md)
- [ScPublicV3ScpGetSpecificContract200Response](docs/Model/ScPublicV3ScpGetSpecificContract200Response.md)
- [ScPublicV3ScpGetUserAuthMetadata200Response](docs/Model/ScPublicV3ScpGetUserAuthMetadata200Response.md)
- [ScPublicV3ScpPatchContract200Response](docs/Model/ScPublicV3ScpPatchContract200Response.md)
- [ScPublicV3ScpPatchReturnsCancel202Response](docs/Model/ScPublicV3ScpPatchReturnsCancel202Response.md)
- [ScPublicV3ScpPatchReturnsCancel409Response](docs/Model/ScPublicV3ScpPatchReturnsCancel409Response.md)
- [ScPublicV3ScpPatchReturnsCancel409ResponseErrorsInner](docs/Model/ScPublicV3ScpPatchReturnsCancel409ResponseErrorsInner.md)
- [ScPublicV3ScpPostCompatShippingOptionsRequest](docs/Model/ScPublicV3ScpPostCompatShippingOptionsRequest.md)
- [ScPublicV3ScpPostPickupRequest](docs/Model/ScPublicV3ScpPostPickupRequest.md)
- [ScPublicV3ScpPostReturnsCreateNewReturn201Response](docs/Model/ScPublicV3ScpPostReturnsCreateNewReturn201Response.md)
- [ScPublicV3ScpPostReturnsCreateNewReturnRequest](docs/Model/ScPublicV3ScpPostReturnsCreateNewReturnRequest.md)
- [ScPublicV3ScpPostReturnsCreateNewReturnSynchronously400Response](docs/Model/ScPublicV3ScpPostReturnsCreateNewReturnSynchronously400Response.md)
- [ScPublicV3ScpPostReturnsCreateNewReturnSynchronously400ResponseError](docs/Model/ScPublicV3ScpPostReturnsCreateNewReturnSynchronously400ResponseError.md)
- [ScPublicV3ScpPostShippingOptions200Response](docs/Model/ScPublicV3ScpPostShippingOptions200Response.md)
- [ScPublicV3ScpPostShippingOptionsSimple200Response](docs/Model/ScPublicV3ScpPostShippingOptionsSimple200Response.md)
- [ScPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber404Response](docs/Model/ScPublicV3ShippingIntelligenceEngineGetGetParcelByTrackingNumber404Response.md)
- [ScPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking409Response](docs/Model/ScPublicV3ShippingIntelligenceEnginePostRegisterParcelForTracking409Response.md)
- [SenderAddressResponse](docs/Model/SenderAddressResponse.md)
- [SenderAddressResponseAllOfSignature](docs/Model/SenderAddressResponseAllOfSignature.md)
- [ServicePoint](docs/Model/ServicePoint.md)
- [ShipWith](docs/Model/ShipWith.md)
- [ShipmentCommon](docs/Model/ShipmentCommon.md)
- [ShipmentCommonWithOptionalFields](docs/Model/ShipmentCommonWithOptionalFields.md)
- [ShipmentCreateRequest](docs/Model/ShipmentCreateRequest.md)
- [ShipmentCreatedResponse](docs/Model/ShipmentCreatedResponse.md)
- [ShipmentRequest](docs/Model/ShipmentRequest.md)
- [ShipmentRequestAsync](docs/Model/ShipmentRequestAsync.md)
- [ShipmentRequestSyncAnnounce](docs/Model/ShipmentRequestSyncAnnounce.md)
- [ShipmentRequestWithOptionalFields](docs/Model/ShipmentRequestWithOptionalFields.md)
- [ShipmentRequestWithRules](docs/Model/ShipmentRequestWithRules.md)
- [ShipmentResponse](docs/Model/ShipmentResponse.md)
- [ShippingDetails](docs/Model/ShippingDetails.md)
- [ShippingOption](docs/Model/ShippingOption.md)
- [ShippingOptionCodeProperties](docs/Model/ShippingOptionCodeProperties.md)
- [ShippingOptionFilter](docs/Model/ShippingOptionFilter.md)
- [ShippingOptionFilterParcelsInner](docs/Model/ShippingOptionFilterParcelsInner.md)
- [ShippingPriceBreakdownInner](docs/Model/ShippingPriceBreakdownInner.md)
- [ShippingProduct](docs/Model/ShippingProduct.md)
- [ShippingProductsRef](docs/Model/ShippingProductsRef.md)
- [ShippingQuote](docs/Model/ShippingQuote.md)
- [ShippingQuotePrice](docs/Model/ShippingQuotePrice.md)
- [ShippingQuoteWeight](docs/Model/ShippingQuoteWeight.md)
- [SingleParcelShippingOptionFilter](docs/Model/SingleParcelShippingOptionFilter.md)
- [Status](docs/Model/Status.md)
- [StrDimensions](docs/Model/StrDimensions.md)
- [StrWeight](docs/Model/StrWeight.md)
- [SyncParcelsArrayResponse](docs/Model/SyncParcelsArrayResponse.md)
- [SyncShipmentResponse](docs/Model/SyncShipmentResponse.md)
- [TaxNumber](docs/Model/TaxNumber.md)
- [TimeSlot](docs/Model/TimeSlot.md)
- [TimeSlotEndAtRequired](docs/Model/TimeSlotEndAtRequired.md)
- [TrackingNumberCreateRequest](docs/Model/TrackingNumberCreateRequest.md)
- [TrackingNumberResponse](docs/Model/TrackingNumberResponse.md)
- [UpdateContractRequest](docs/Model/UpdateContractRequest.md)
- [UpsPickupAddress](docs/Model/UpsPickupAddress.md)
- [UpsPickupItem](docs/Model/UpsPickupItem.md)
- [UpsPickupRequest](docs/Model/UpsPickupRequest.md)
- [UpsPickupResponse](docs/Model/UpsPickupResponse.md)
- [UserAuthMetadata](docs/Model/UserAuthMetadata.md)
- [ValidationError](docs/Model/ValidationError.md)
- [Volume](docs/Model/Volume.md)
- [VolumeUnits](docs/Model/VolumeUnits.md)
- [Weight](docs/Model/Weight.md)
- [WeightUnit](docs/Model/WeightUnit.md)
- [WeightUnits](docs/Model/WeightUnits.md)

## Authorization

### HTTPBasicAuth

- **Type**: HTTP basic authentication


### OAuth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **api**: Full API access


### OAuth2

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://account.sendcloud.com/oauth2/auth`
- **Scopes**: 
    - **api**: Full API access

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

contact@sendcloud.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `3.0.0`
    - Package version: `0.3.0`
    - Generator version: `7.18.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
