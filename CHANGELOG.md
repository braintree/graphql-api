# 01-29-2024

* Delete / Deprecate field
    * `phoneNumber` from `AddressInput`
    * `bankAccount` from `MerchantAccount` 
* Add new field
    * `acquirerCountryCode` to `MetaCheckoutConfiguration`
    * `merchantAccountId` to `TokenizeNetworkTokenPayload`

# 01-16-2024

* Add new docstring for date in `transactionLevelFees` and `paymentLevelFees` under the `Report` type

# 01-02-2024

* Add new field
    * `phoneNumber` to `AddressInput`
    * `dateOfBirth` and `countryCode` to `IndustryFlightInput`
    * `implicitlyVaultedPaymentMethodId` to `LocalPaymentDetails`
    * `errors` to `RequestAuthorizeInStoreContext` and `RequestChargeInStoreContext`
    * `surchargeAmount` and `processingMode` to `Transaction`
    * `surchargeAmount` to `TransactionInput`
    * `shippingMethod` to `TransactionShipping` and `TransactionShippingInput`
    * `verificationAddOns` to `VaultUsBankAccountInput` and `VerifyUsBankAccountInput`
* Update doc string
    * `skipCvv` and `skipAvs` in `CreditCardDetails`
    * `legs` in `IndustryFlightInput`
* Delete field
    * `initiatedBy`, `deleteRelatedPaymentMethods`, and `fraudRelated` from `DeletePaymentMethodFromVaultInput`
* Add new value
    * `UNDER_REVIEW` to `DisputeStatus` enum
    * `TRUSTLY` to `NonInstantLocalPaymentMethodType` enum
    * `INSTALLMENT` and `INSTALLMENT_FIRST` to `PaymentInitiator` enum
* Add new object
    * `InStoreContextError` type
    * `ProcessingMode` enum
    * `TransactionShippingMethod` enum
    * `UsBankAccountVerificationAddOn` enum
* Update type
    * `InStoreReader`


# 10-31-2023 🎃

* Add new mutation
    * `updateCreditCardCardholderName`
* Add new input
    * `UpdateCreditCardCardholderNameInput`
* Add new type
    * `UpdateCreditCardCardholderNamePayload`

# 10-24-2023

* Add field
    * `industry` for `CaptureTransactionOptionsInput`, `InStoreAuthorizationInput`, `InStoreTransactionInput`, `PartialCaptureTransactionOptionsInput`, `TransactionInput`
* Deprecate
    * `evidenceSubmittable` for `Dispute`
    * `updateTransactionCustomFields` mutation
    * `UpdateTransactionCustomFieldsInput`
    * `UpdateTransactionCustomFieldsPayload`
* Add new input
    * `IndustryAdditionalChargeInput`
    * `IndustryCruiseInput`
    * `IndustryFlightInput`
    * `IndustryFlightLegInput`
    * `IndustryLodgingInput`
    * `TransactionIndustryInput`
    * `UpdateCustomFieldsInput`
* Add new enum
    * `IndustryAdditionalChargeType`
    * `IndustryCruiseTravelPackageType`
* Update doc strings for `InStoreContextStatus` enum values
* Update `InStoreLocation` type to implement `Node` interface
* Add new mutation
    * `updateCustomFields`
* Add new type
    * `UpdateCustomFieldsPayload`

# 10-10-2023

* Remove deprecation
    * `merchantAccountId` for `CreditCardVerificationOptionsInput`
* Add new mutation with assocaited input and payload
    * `updateCreditCardExpirationDate`
* Add new field / value
    * `paymentMethod` for `UpdateCreditCardBillingAddressPayload`
* Deprecate
    * `billingAddress` for `UpdateCreditCardBillingAddressPayload`

# 10-03-2023

* Add new field / value
    * `metaCheckout` for `ClientConfiguration`
    * `MetaCheckoutOriginDetails` for `PaymentMethodOriginDetails` union
    * `META_CHECKOUT` to `PaymentMethodOriginType`
    * `CREDIT_CARD_VIA_META_CHECKOUT` to `PaymentMethodShapshotSearchType` enum
    * `selectedFinancingOption` for `PayPalAccountDetails`
    * `statusReason` for `RequestAuthorizeInStoreContext` and `RequestChargeInStoreContext`
    * `processingOverrides` for `TransactionInput`
    * `threeDSecureAuthenticationId` for `VaultCreditCardInput` and `VaultPaymentMethodInput`
* Deprecate
    * `PARTIALLY_COMPLETE` value for `InStoreContextStatusi`
    * `privacyUrl` for `PayPalConfiguration`
    * `userAgreementUrl` for `PayPalConfiguration`
* Add new enum
    * `InStoreTransactionContextStatusReason`
* Add new type
    * `MetaCheckoutConfiguration`
    * `MetaCheckoutOriginDetails`
* Add new input
    * `TransactionProcessingOverridesInput`


# 08-08-2023

* Update schema descriptions for clearer documentation
* Add new enum
  * `CreditCardCustomerLocation` for `SearchCreditCardCustomerLocationInput`
  * `ThreeDSecureDeviceChannel` for `ThreeDSecureDetails`
* Add new input
  * `SearchCreditCardLocationInput`
  * `ThreeDSecureLookupBrowserInformationInput
* Add new field
  * `customerLocation` to `SearchPaymentCreditCardDetailsInput`
  * `browserInformation` to `ThreeDecureLookupTransactionInformationInput`
  * `deviceChannel` to `ThreeDSecureLookupTransactionInformationInput`

# 06-27-2023

* Deprecate `AVS_RESPONSE` enum value for `DisputeEvidenceCategory` and `DisputeTextEvidenceCategory` enum.

# 06-20-2023

* Remove `ConfirmationPromptAlignment` enum.
* Add new enum
    * `DecimalPlaces` enum for `CustomFieldName`.
    * `InStoreReaderDisplayAlignment` enum to `InStoreReaderConnectionEdge` type.
    * `InStoreReaderTextPromptType` enum to `InStoreReaderSetupInput` input.
* Add new input
    * `InStoreAuthorizationInput`
    * `RequestAmountPromptFromInStoreReaderInput`
    * `RequestAuthorizeFromInStoreReaderInput`
    * `RequestNonPciCardDataFromInStoreReaderInput`
    * `RequestTextPromptFromInStoreReaderInput`
* Add new mutation
    * `requestAuthorizationFromInStoreReader`
    * `requestNonPciCardDataFromInStoreReader`
    * `requestAmountPromptFromInStoreReader`
    * `requestTextPromptFromInstoreReader`
* Add new union
    * `NonPciCardData`
* Add new type
    * `NonPciFinancialCardMagneticStripeData`
    * `RequestAmountPromptInStoreContext`
    * `RequestAuthorizeInStoreContext`
    * `RequestNonPciCardDataInStoreContext`
    * `RequestTextPromptInStoreContext`
* Add new field
    * In `RequestSignaturePropmtFromInStoreReaderInput`
        * `waitForNextRequest`
        * `displayTimeout`
    * In `RequestTextDispalyFromInStoreReaderInput`
        * `title`
        * `alignment`
        * `waitForNextRequest`
        * `displayTimeout`
* Deprecate `reason` for `RefundInput`
* Change type of `alignment` field in `RequestConfirmationPromptFromInStoreReaderInput` to `InStoreReaderDisplayAlignment`

# 06-14-2023

* Add `retiredParentTransaction` field to `Transaction` type
* Add `retriedTransactions` field to `Transaction` type

# 06-06-2023

* Add `ClientSDKMetadata` type.
* Add `CreateVenmoPaymentContextInput` input.
* Add `CustomerClient` enum.
* Add `MerchantAdviceCodeResponse` type
* Add `merchantAdviceCodeResponse` field to `FailedEvent`, `GatewayRejectedEvent`, and `ProcessorDeclinedEvent`.
* Add `createVenmoPaymentContext` mutation.
* Add `PaypalLineItem` type.
* Add `enrichedCustomerDataEnabled` field for `VenmoConfiguration`.
* Add `VenmoIntent` enum.
* Add `VenmoPaymentContext` type.
* Add `VenmoPaymentContextPayload` type.
* Add `VenmoPaymentContextStatus` enum.
* Add `VenmoPaysheetDetails` type.
* Add `VenmoPaysheetDetailsInput` input.
* Add `VenmoPaysheetTransactionDetails` type.
* Add `VenmoPaysheetTransactionDetailsInput

# 05-23-2023

* Add `userName` field to `AuthorizedEvent`, `FailedEvent`, `GatewayRejectedEvent`, `ProcessorDeclinedEvent`, `SettlementPendingEvent`, `SubmittedForSettlementEvent`, `VoidedEvent`.
* Add `completedAt` and `submittedAt` fields to `BusinessAccountCreationRequest`.
* Increase the maximum of `installmentCount` to 48.
* Add `fax` and `website` fields to `Customer` and `CustomerInput`.
* Add `evidenceSubmittable` field to `Dispute`.
* Add `AUTO_ACCEPTED` to DisputesStatus enum.
* Add `CARRIER_NAME`, `GENERAL`, `REFUND_ID`, and `TRACKING_NUMBER` to `DisputeTextEvidenceCategory` enum.
* Add `PARTIALLY_COMPLETE` to `InStoreContextStatus` enum.
* Add `purchaseOrderNumber`, `tax`, `shipping`, `discountAmount`, and `lineItems` fields to `InStoreTransactionInput`.
* Add `shippingAddress`, `billingAddress`, `disputeReceivedDate`, and `processorAuthorizationId` to `PaymentSearchInput`, RefundSearchInput`, and `TransactionSearchInput`.
* Add `requestedExemptionType` to `PerfomrThreeDSecureLookupInput`.
* Add `company`, `addressLine1`, `addressLine2`, `firstName`, `lastName`, `adminArea1`, `adminArea2`, `postalCode`, and `countryName` fields to `Search`.
* Add `fax`, `phone`, and `website` fields to `SearchPaymentCustomerInput`.
* Deprecate `email` under `SearchPaymentPayPalDetailsInput`.
* Add `payerEmail`, `authorizationId`, and `paymentId` to `SearchPaymentPayPalDetailsInput`.
* Add `required` to `ThreeDSecureAuthenticationInput`,
* Add `EXEMPTION_LOW_VALUE_SUCCESSFUL` , `EXEMPTION_TRA_SUCCESSFUL`, `MPI_SERVER_ERROR`, and `SKIPPED_DUE_TO_RULE` to `ThreeDSecureAuthenticationStatus` enum.
* Remove `UNKNOWN` from `UsBankAccountType` enum.
* Add `makeDefault` and `failOnDuplicatePaymentMethod` fields to `VaultCreditCardInput`.
* Add `makeDefault` field to `VaultLimitedUsePayPalAccountOptionsInput`, `RiskDataInput`, and `VaultUsBankAccountInput`.

# 12-08-2022

* Remove `PayPalExperienceProfileInput` from `CreatePayPalBillingAgreementInput`.
* Add  `PayPalBillingAgreementExperienceProfileInput` to `CreatePayPalBillingAgreementInput`. 
* Add `paypalProductAttributes` to `CreatePayPalBillingAgreementInput`.
* Add `preDisputeProgram` to `Dispute`.
* Add `SearchPreDisputeProgramInput` to `DisputeSearchInput`.
* Add `PayPalBillingAgreementChargePattern` enum.
* Add `PayPalUserAction` field to `PayPalExperienceProfileInput` 

# 11-10-2022

* Add `paymentInitiatedAt` to Refund.
* Add `authorizationExpiredAt`, `authorizedAt`, `gatewayRejectedAt`, `processorDeclinedAt` to `SearchPaymentStatusTransitionInput`.

# 10-13-2022

* Update `Language` scalar docstring.

# 10-03-2022

* Add `PAY_UPON_INVOICE' to `LocalPaymentMethodType` enum.
* Add `PAY_UPON_INVOICE_VIA_PAYPAL` to `PaymentMethodSnapshotSearchType` enum.

# 09-30-2022

* Add 255 character limit to the `clientMutationId` field.
* Add fields to `DeletePaymentMethodFromVaultInput`.
* Deprecate `ChargebackProtectionLevel` under `Dispute`.
* Add `protectionLevel` to `Dispute`.
* Add `DisputeProtectionLevel` enum.
* Add `protectionLevel` to `DisputeSearchInput`.
* Add `EXCESSIVE_RETRY` to `GatewayRejectedEvent` enum
* Remove `PARTIALLY_COMPLETE` from `InStoreContextStatus` enum.
* Add `vaultPaymentMethodAfterTransacting` field to `InStoreTransactionInput.
* Add `liabilityShift` to `RiskData` type.
* Add `GRABPAY` and `SATISPAY` to `LocalPaymentMethodType` enum.
* Add support for the `sepaDirectDebit` payment method.
* Add `tokenizePayPalOneTimePayment` mutation.
* Add `createPayPalOneTimePayment` mutation.
* Remove `createKlarnaEUSession` mutation.
* Remove `updateKlarnaEUSession` mutation.
* Remove `updateKlarnaEUOrderShippingInfo` mutation.
* Add `requestSignaturePromptFromInStoreReader` mutation.
* Remove `createAfterpayAUNZCheckout` mutation.
* Add `requestConfirmationPromptFromInStoreReader` mutation.
* Update Docstring for `PaymentInitiator` enum.
* Add `GRABPAY_VIA_PAYPAL`, `SATISPAY_VIA_PAYPAL`, and `SEPA_DIRECT_DEBIT` to `PaymentMethodSnapshotSearchType` enum.
* Add `shippingAddress` to `PayPalAccountDetails`.
* Add `description` and `reason` fields to `PayPalRefundDetails`.
* Update Docstring for `report` and `search` queries.
* Add `description` and `reason` to `RefundInput`.
* Add `settlementState` to `SandboxSettleTransactionInput`.
* Add deprecation note to `SearchChargebackProtectionLevelInput` Docstring,
* Add `SearchDisputeProtectionLevelInput`
* Add `retried` field to `Transaction`.
* Update Docstring for `paymentInitiator` field under `TransactionInput`.
* Update regex validation and Docstring for `URL` docstring.

# 2022-03-02

* Add `softwareVersion` and `readerStatus` to `InStoreReaderSearchInput`.
* Undeprecate `SETTLEMENT_CONFIRMED` in `PaymentStatus`, it will be present on partially captured transactions.
* Add `SettlementConfirmedEvent` as an implementation of the `PaymentStatusEvent` interface.
* Add `serialNumber` to `VerifoneVendor`.

# 2022-02-08

* Add `PARTIALLY_COMPLETE` to `InStoreContextStatus` enum.
* Add `VAULT` to `PaymentReaderInputMode` enum.
* Add `PAYMENT_READER` to `PaymentSource` enum to allow searching for payments originated at a reader.

# 2021-12-21

* Add `PAYMENT_CONTEXT` to `LegacyIdType` enum.
* Add `legacyId` to `LocalPaymentContext`.
* Add `tokenizePayPalBillingAgreement`, `createPayPalBillingAgreement`, and `updateInStoreReader` mutations.
* Add `inStoreReaders` search query.
* Add `customerDetails` on `TransactionInput`.

# 2021-10-14

* Add `LOOKUP_CARD_ERROR` and `LOOKUP_SERVER_ERROR` to `ThreeDSecureAuthenticationStatus`.

# 2021-10-07

* Update `expiryDate` docstring in `NonInstantLocalPaymentContextInput`.

# 2021-09-16

* Add `createNonInstantLocalPaymentContext` mutation.
* Add `UNKNOWN` to `UsBankAccountType`.

# 2021-09-09

* Add `VenmoPayerInfoInput` to `ApproveVenmoPaymentContextInput`.
* Add `VenmoPayerInfo` type.  
* Add `NonInstantLocalPaymentType` enum.
* Add `MULTIBANCO` to `LocalPaymentMethodType` enum. 
* Update `createDisputeFileEvidence` docstring.

# 2021-08-19

* Add `channel` to `InStoreTransactionInput`.

# 2021-08-12

* Add `accountBalance` to `CreditCardTransactionDetails`.
* Add `expiredAt` and `orderId` to `LocalPaymentContext`.
* Add new payment method types to `PaymentMethodSnapshotSearchType`.
* Add `cardAdd` to `PerformThreeDSecureLookupInput`.
* Add `initialRequestedAuthorizationAmount` to `Transaction`.
* Add `encryptionKey` to `VisaCheckoutConfiguration`.
* Update `LocalPaymentContext.type` to `LocalPaymentMethodType` enum.

# 2021-08-05

* Add `inStoreLocations` query.
* Add `businessAccountCreationRequests` to `Search`.

# 2021-07-22

* Add `BOLETOBANCARIO` and `OXXO` to `LocalPaymentMethodType`.

# 2021-07-15

* Add `generateExchangeRateQuote` mutation.
* Add `disbursementDetails` to `Refund`.
* Add `transactionId` to `ThreeDSecureLookupData`.
* Add `exchangeRateQuoteId` to `TransactionInput`.

# 2021-06-24

* Add `requestFirmwareUpdateFromInStoreReader` mutation.
* Add `cardOnFileNetworkTokenized` to `CreditCardDetails`.
* Add `processedWithCardOnFileNetworkToken` to `CreditCardTransactionDetails`.

# 2021-06-17

* Add `updateInStoreLocation` mutation.
* Add `dbaName`, `externalId`, `hyperwalletAccount`, and `venmoAccount` to `MerchantAccount`.
* Add `appUsedForScanning` to `PayPalTransactionDetails`.
* Add `paymentInitiatedAt` to `Transaction`.
* Add `merchantAccountId` input to `UpdateCreditCardBillingAddressInput`.
* Change `verification` on `UpdateCreditCardBillingAddressInput` to `CreditCardVerificationOptionsInput` and add additional inputs.
* Add `skip` and `fraudTools` inputs to `CreditCardVerificationOptionsInput`.
* Add `fraudTools` input to `VaultCreditCardVerificationOptionsInput`.

# 2021-05-28

* Add `updateTransactionAmount` mutation.

# 2021-05-13

* Add `createDisputeFileEvidence`, `requestVaultFromInStoreReader`, `requestTextDisplayFromInStoreReader`, `requestItemDisplayFromInStoreReader`, `createKlarnaEUSession`, `updateKlarnaEUSession`, `updateKlarnaEUOrderShippingInfo`, and `createAfterpayAUNZCheckout` mutations.
* Add `pingInStoreReader` query.
* Add `installmentCount` to `CreditCardTransactionOptionsInput`.
* Add `taxIdentifiers` to `CustomerInput`.
* Add `chargebackProtectionLevel` to `Dispute`.
* Add `chargebackProtectionLevel` to `DisputeSearchInput`.
* Add `CHARGEBACK_PROTECTION`, `EFFORTLESS_CHARGEBACK_PROTECTION`, and `FRAUD_PROTECTION_ADVANCED` to `FraudServiceProvider` enum.
* Add `countryCode` to `GooglePayConfiguration`.
* Add `InStoreContextResult` interface.
* Add `id`, `reader`, and `status` to `InStoreContextPayload`.
* Add `payerId` and `enableQRCodePayments` to `InStoreLocationInput`.
* Add `merchantAccounts` to `Merchant`.
* Add `bankAccount`, `paypalAccount`, `threeDSecure` to `MerchantAccount`.
* Make `eCommerceIndicator` nullable on `NetworkTokenInput`.
* Add non-nullable `originDetails` to `NetworkTokenInput`.
* Add `MANUAL_KEY_ENTRY` to `PaymentReaderInputMode` enum.
* Add `storeId` to `PaymentSearchInput`, `RefundSearchInput`, and `TransactionSearchInput`
* Add `dataOnlyRequested` to `PerformThreeDSecureLookupInput`.
* Add `decisionReasons` and `score` to `RiskData`.
* Add `DATA_ONLY_SUCCESSFUL` and `UNSUPPORTED_ACCOUNT_TYPE` to `ThreeDSecureAuthenticationStatus` enum.
* Add `installmentDetails` to `Transaction`.
* Change `rights` on `Viewer` to return `[Right!]`.
* Deprecate all fields on `InStoreContext`.
* Deprecate `inStoreContext` on `InStoreContextPayload`, use top-level fields instead.

# 2021-02-26

* Add `createUniversalAccessToken` mutation.
* Add `internalName`, `geoCoordinates`, `payerId` and `qrCodePaymentsEnabled` to `InStoreLocation`.
* Add `internalName`, `geoCoordinates`, `payerId` and `enableQRCodePayments` to `InStoreLocationInput`.
* Add `merchantAccountId` to `RefundInput`.
* Add `rights` to `Viewer`.

# 2021-02-11

* Use `CountryCode` instead of `CountryCodeAlpha3` to expand accepted ISO formats.
* The `verification` field on `VaultCreditCardInput` is now `VaultCreditCardVerificationOptionsInput` to allow credit card specific options.
* The `category` field on `DisputeEvidence`, `DisputeFileEvidence`, and `DisputeTextEvidence` is now `DisputeEvidenceCategory` scalar instead of a `String`.
* Add `CITI` value to `CreditCardBrandCode` enum.
* Add mutation `createDisputeTextEvidence` to allow associating text evidence to a dispute.
* Add mutation `deleteDisputeEvidence` to allow deleting evidence from a dispute.
* Add mutation `finalizeDispute` to allow finalizing an open dispute.
* Add mutation `requestRefundFromInStoreReader`.
* Add mutation `removeCreditCardFromAccountUpdater`.
* Add `vaultPaymentMethodAfterTransacting` field to `TransactionInput` to allow automatically vaulting a single-use payment method after charging it.
* Add `threeDSecurePassThrough` field to `VaultCreditCardInput` to return merchant-performed 3D Secure authentication results.
* Add `paymentMethodIds` field and deprecate `paymentMethodId` to `SubmitCreditCardForAccountUpdaterInput` to allow multiple payment methods at a time.
* Add `content` field to `DisputeTextEvidence`, and deprecate the `comment` field.
* Add `amount` field to `CreditCardVerificationOptionsInput` to allow verifying credit cards for a particular amount.
* Add `directoryServerTransactionId` field to `ThreeDSecurePassThroughInput` (and correct documentation for `threeDSecureServerTransactionId`).
* Add `refund` field to `InStoreContext`.
* Add `customFields` and `descriptor` fields to `Refund`.
* Add `customFields` and `descriptor` fields to `DetachedRefundInput`.

# 2021-01-14

* Support SCA exemptions by adding `scaExemption` input field to `CreditCardTransactionOptionsInput` and `scaExemptionRequested` field to `Transaction`.
* Add values to `ThreeDSecureAuthenticationStatus` enum.
* Deprecate `AUTHENTICATE_SUCCESSFUL_ISSUER_NOT_PARTICIPATING` in `ThreeDSecureAuthenticationStatus` enum.

# 2020-12-21

* Add `paymentMethodSnapshot` field to `Payment` interface.
* Add `LOCAL_PAYMENT` value to `PaymentMethodSnapshotSearchType`.
* Rename `PaymentPaymentMethodSearchInput` to `SearchPaymentPaymentMethodInput`.
* Add `paymentMethodSnapshot` input to `SearchPaymentPaymentMethodInput`.

# 2020-12-10

* Add `addressLine1`, `addressLine2`, `adminArea2`, and `adminArea1` to `AddressInput`.

# 2020-12-03

* Add `SWITCH` value to `CreditCardBrandCode` enum.
* Add `userId` input to `PaymentSearchInput`, `TransactionSearchInput` and `RefundSearchInput`.
* Add `phoneNumber` field to `Address`.
* Add `merchantId`, `merchantName`, and `merchantAddress` fields to `Transaction`.

# 2020-11-19

* Rename `SearchCustomerInput` input type to `SearchPaymentCustomerInput`.
* Add additional fields to `SearchPaymentCustomerInput` to allow searching for Payments by more customer details.
* Add `ELO` value to `CreditCardBrandCode` enum.
* Update `Address` type with global field names.

# 2020-11-12

* Add `HIPERCARD` and `HIPER` values to `CreditCardBrandCode` enum.
* Add `merchantAccounts` field to the `Merchant` type, allowing retrieval of a list of merchant accounts via the `viewer` query.
* Add `paypalFinancingOptions` query to return PayPal financing options, along with associated inputs, types, and scalars.
* Add `selectedFinancingOption` field to `ChargePayPalAccountOptionsInput` to provide PayPal financing options on `chargePayPalAccount` mutation.
* Add `selectedFinancingOption` field to `PayPalTransactionDetails` to return PayPal financing options.
* Deprecate `currencyIsoCode` field name in favor of `currencyCode`.
* Deprecate `clientMutationId` field on query payloads.

# 2020-11-05

* Add `acquirerReferenceNumber` to `CreditCardTransactionDetails`.
* Add `descriptor` to `PartialCaptureTransactionOptionsInput`.
* Add `limitedUseOrderId` to `PayPalAccountDetails`.
* Add `requestChargeFromInStoreReader` and `requestCancelFromInStoreReader` mutations.

# 2020-10-29

* Add `customer` field to `PaymentSearchInput` and `RefundSearchInput`, allowing searching for Payments and Refunds by customer information.
* Add `phone` field, representing a phone number, to `PayPalAccountDetails`.

# 2020-10-15

* Add `settlementBatchId` and `paymentMethod` fields to `TransactionSearchInput`, `PaymentSearchInput`, and `RefundSearchInput`.

# 2020-10-07

* Change type of `CreditCardDetails.threeDSecure` from `ThreeDSecureAuthentication` to `ThreeDSecureDetails`.
* Add `emvData` to `TransactionAuthorizationProcessorResponse`.
* Add `imageUrl` to `TransactionLineItemInput` and `TransactionLineItem`.

# 2020-10-01

* Add `fraudTools` and `threeDSecureAuthentication` to `CreditCardTransactionOptionsInput`.
* Add `tokenizedCvv` to `CreditCardVerificationOptionsInput`.
* Add `merchantAccountId` to `DeletePaymentMethodFromVaultPayload`.
* Add `refundUsBankAccount` mutation.
* Deprecate `threeDSecurePassThrough` on `TransactionInput`.

# 2020-09-22

* Add `riskData` field to `CreditCardVerificationOptionsInput`, `VaultCreditCardInput`, and `VaultPaymentMethodInput`.

# 2020-09-03

* Add `tokenizedCvv` to `CreditCardTransactionOptionsInput`.
* Add `FRAUD_PROTECTION_ENTERPRISE` to `FraudServiceProvider` enum.
* Add `tokenizedCvv` to `TokenizeCvvPayload`.
* Add `authorizationAdjustments` to `Transaction`.
* Change `authorizePayPalAccount` and `chargePayPalAccount` to return `PayPalTransactionPayload` instead of `TransactionPayload`.
* Deprecate `singleUseToken` on `TokenizeCvvPayload`.

# 2020-08-24

* Add `name` field to `OAuthApplication`.
* Add `origin` field to `PayPalAccountDetails` and `PayPalTransactionDetails`.
* Add `retrievalReferenceNumber` field to `TransactionAuthorizationProcessorResponse`.

# 2020-08-19

* Add `CardAccountType` enum.
* Add `accountType` field to `CreditCardTransactionDetails`.
* Add `accountType` field to `CreditCardTransactionOptionsInput`.
* Add `accountType` and `billingAddress` fields to `VaultCreditCardInput`.
* Add `verifyCreditCard` mutation.
* Add `settlementBatchId` field to `SettledEvent`.

# 2020-08-12

* Add `billingAddress` to `CreditCardTransactionOptionsInput`.

# 2020-08-05

* Add `discountAmount`, `lineItems`, `purchaseOrderNumber`, `shipping`, and `tax` fields to `CaptureTransactionOptionsInput` and `PartialCaptureTransactionOptionsInput`.
* Add `refundCreditCard` mutation.
* Add `paymentInitiator` to `TransactionInput`.
* Deprecate `recurring` field on `TransactionInput`.

# 2020-07-20

* Fix `processorResponse` deprecation reason. Fixes [#13](https://github.com/braintree/graphql-api/issues/13)

# 2020-07-15

* Add `billingAddress` to `CreditCardDetails`, `TokenizeNetworkTokenInput`.
* Add `updateCreditCardBillingAddress` mutation.
* Add `itemType` to `TransactionLineItem`, `TransactionLineItemInput`.
* Rename `VaultPaymentMethodVerificationOptionsInput` to `PaymentMethodVerificationOptionsInput`.

# 2020-07-09

* Add additional values to `GatewayRejectionReason` enum.
* Add `lineItems` to `Refund` and `RefundInput`.

# 2020-07-01

* Add `networkResponse` field to various relevant `PaymentStatusEvent` types.
* Add `networkResponse` field to `Verification`.
* Add `additionalInformation` field to `VerificationProcessorResponse`.

# 2020-06-08

* Add `additionalInformation` to `TransactionAuthorizationProcessorResponse`.

# 2020-06-05

* Add `authorizeCreditCard` mutation.
* Add `chargeCreditCard` mutation.
* Add `vaultCreditCard` mutation.
* Support external vault information via `TransactionExternalVaultOptionsInput` in the above credit card mutations.
* Add `CreditCardTransactionDetails` `PaymentMethodSnapshot` union member to eventually replace `CreditCardDetails` on transaction payment method snapshot.

# 2020-05-13

* Remove unused `clientId` and `serialNumber` from `GenerateInStoreReaderPairingCodeInput`.
* Add `deviceId` to `GenerateInStoreReaderPairingCodeInput`.
* Add new query `preferredPaymentMethods`.

# 2020-05-05

* Add support for in-store locations and card readers.

# 2020-04-15

* Add `customerAuthenticationIndicator` to `AuthenticationInsight`.
* Add `amount`, `recurringCustomerConsent`, and `recurringMaxAmount` fields to `AuthenticationInsightInput`.
* Add `authorizationExpiresAt` field to `AuthorizedEvent`.
* Add `riskContext` to `AuthorizePayPalAccountOptionsInput` and `ChargePayPalAccountOptionsInput`.
* Add `fraudProvider` to `ClientConfiguration`.
* Deprecate `kount` field in `ClientConfiguration`.
* `CustomActionsPaymentContext` now implements `Node` interface.
* Add `updatedAt` to `CustomActionsPaymentContext`.
* Add `CustomerAuthenticationIndicator` enum.
* Add `RBI` to `CustomerAuthenticationRegulationEnvironment` enum.
* Add `FraudProviderConfiguration` type.
* Add `PayPalAccountInput`.
* Add `PayPalTransactionRiskContextDataFieldInput`.
* Add `PayPalTransactionRiskContextInput`.
* Add `indirectPayee` field to `VaultPayPalBillingAgreementInput`.

# 2020-04-01

* Remove unused `merchantAccountId` input field from `CreateCustomActionsPaymentContextInput`.

# 2020-03-09

* Add new mutation `createCustomActionsPaymentContext`.
* Add `paymentMethodSnapshot`, `paymentMethod`, and `customer` fields to `Refund`.
* Allow searching for `payments` by `type`, `disbursementDate`, `source`, and `facilitatorOAuthApplicationClientId`.
* Allow searching for `refunds` by `merchantAccountId`, `disbursementDate`, `source`, and `facilitatorOAuthApplicationClientId`.
* Allow searching for `transactions` by `merchantAccountId`.
* Model detached refunds as `Refund`.

# 2020-02-27

* Add `fullName` field to `Address`.
* Deprecate `Address.firstName` and `Address.lastName` in favor of `Address.fullName`.
* Add `billingAddress` field to `PayPalAccountDetails`.
* Add `cobrandedCardLabel` field to `PayPalAccountDetails`.

# 2020-02-14

* Add `LocalPaymentDetails` to `PaymentMethodSnapshot` union to support transactions with local payments.
* Add `PayPalLocalPaymentOriginDetails` to `PaymentMethodOriginDetails` union.
* Add `PayPalLocalPaymentRefundDetails` to `RefundPaymentMethodDetails` union.
* Add `PAYPAL` to `PaymentMethodOriginType` enum.
* Add `AUTHENTICATE_SUCCESSFUL_ISSUER_NOT_PARTICIPATING` to `ThreeDSecureAuthenticationStatus`.
* Add additional input fields to `ThreeDSecureLookupTransactionInformationInput`.
* Add `Payment` interface to represent the movement of money by `Transaction` or `Refund`.
* Rename `TransactionSource` enum to `PaymentSource`.
* Rename `TransactionStatus` enum to `PaymentStatus`.
* Rename `TransactionStatusEvent` interface to `PaymentStatusEvent`.
* Add `paymentLevelFees` field to `Report` type as an alias of `transactionLevelFees`, `transactionLevelFees` already returned a report that included transactions and refunds.
* Add `payments` field to `Search` type to allow searching for all types implementing `Payment`.
* Make `supportedCardBrands` list entries non-nullable.
* Make `supportedFeatures` list entries non-nullable.
* Make `challenges` list entries non-nullable.

# 2019-12-18

* Add `reverseRefund` mutation.
* Add `details` field to `Refund`.
* Deprecate `PayPalTransactionDetails.refundId`. Use `Refund.details.refundId` instead.
* Add `disbursementDetails` field to `Transaction`.
* Add `disbursementDate` field to `TransactionSearchInput`.

# 2019-12-05

* Add `sandboxSettleTransaction` mutation.
* Add `createdAt` field to `PaymentMethod`.
* Add `achMandate` field to `UsBankAccountDetails`.

# 2019-11-19

* Split `TransactionProcessorResponse` into `TransactionAuthorizationProcessorResponse` and `TransactionSettlementProcessorResponse`. Transaction status events related to authorization now reference the former and those related to settlement now reference the latter in their `processorResponse` field.
* Add `authorizationId` field to `TransactionAuthorizationProcessorResponse`.
* Add `legacyId` field to `DisputeEvidence` interface and implementations.
* Add `merchantAccountId` search field to `DisputeTransactionSearchInput`.

# 2019-11-07

* Add `customers` search field to `Search` query (fixes [#4](https://github.com/braintree/graphql-api/issues/4)).
* Add `verifications` search field to `Search` query.
* Add `disputes` search field to `Search` query.
* Add `acceptDispute` mutation.
* Add `referenceNumber` and `replyByDate` fields to `Dispute`.
* Add `effectiveDate` to `DisputeStatusEvent`.
* Add `AUTHENTICATE_REJECTED`, `AUTHENTICATION_BYPASSED`, and `CHALLENGE_REQUIRED` statuses to `ThreeDSecureAuthenticationStatus` enum.
* Add `DISPUTE` and `US_BANK_ACCOUNT_VERIFICATION` to `LegacyIdType` enum.
* Add `vaultPayPalBillingAgreement` mutation to import and vault an existing PayPal Billing Agreement that was not created through Braintree.
* Add `source` and `facilitatorDetails` fields to `Transaction`.
* Allow searching for transactions by source and facilitator details.
* Deprecate `transactionFeeAmount` and `transactionFeeCurrencyIsoCode` fields on `PayPalTransactionDetails` in favor of `transactionFee` on `PayPalTransactionDetails`.

# 2019-10-15

* Deprecate `countryCodeAlpha3`, `countryCodeAlpha2`, `countryCodeNumeric` and `countryName` on `AddressInput`, use `countryCode` instead.
* Deprecate `payee` on `AuthorizePayPalAccountOptionsInput` and `ChargePayPalAccountOptionsInput`.
* Return data in the `threeDSecure` field on `CreditCardDetails` when present and `CreditCardDetails` are returned as part of the `PaymentMethodSnapshot` union.
* Add `updateTransactionCustomFields` mutation.

# 2019-10-03

* Add `Dispute` type.
* Add `dispute` field to `Transaction` to retrieve all of a transaction's disputes.
* Add `threeDSecurePassThrough` to `TransactionInput` (fixes [#3](https://github.com/braintree/graphql-api/issues/3)).
* Add `verification` field to `VaultPaymentMethodInput`.
* Add support for opting-out of verifications when vaulting a payment method via the `vaultPaymentMethod` mutation.
* Deprecate `VaultPaymentMethodInput.verificationMerchantId`, use `VaultPaymentMethodInput.verification.merchantAccountId` instead.
* Update `PageInfo` to include all [Relay required fields](https://facebook.github.io/relay/graphql/connections.htm#sec-undefined.PageInfo).

# 2019-09-12

* Add `threeDSecure` field to `CreditCardDetails`.
* Add `authorizePayPalAccount` mutation.
* Add `authorizeVenmoAccount` mutation.
* Add `tokenizeNetworkToken` mutation.
* Add `performThreeDSecureLookup` mutation.
* Add `NetworkTokenOriginDetails` to `PaymentMethodOriginDetails` union.
* Add `NETWORK_TOKEN` to `PaymentMethodOriginType` enum.
* Add `CREDIT_CARD_VIA_NETWORK_TOKEN` to `PaymentMethodSnapshotSearchType` enum.

# 2019-08-28

* Add `vaultUsBankAccount` mutation.
* Add `verifyUsBankAccount` mutation.
* Add `confirmMicroTransferAmounts` mutation.
* Add `partialCaptureTransaction` mutation.
* Add `partialCaptureDetails` field to `Transaction`.
* Deprecate `amount` field on `Verification` in favor of `paymentMethodVerificationDetails` which includes payment method specific information.
* Add `PENDING` and `VERIFYING` to `VerificationStatus`.

# 2019-08-14

* Fix some documentation typos.

# 2019-08-09

* Add `paymentMethodSnapshotType` to `TransactionSearchInput` to support searching for transactions by payment method type.

# 2019-08-02

* Add `AuthenticationInsight` type and corresponding field to `TokenizeCreditCardPayload`.

# 2019-07-31

* Add `transaction` field to `CaptureTransactionInput`.
* Add ability to pass `descriptor` and `orderId` when capturing a transaction.
* Deprecate `amount` field on `CaptureTransactionInput` in favor of `amount` field on `CaptureTransactionOptionsInput`.

# 2019-07-29

* Add `refunds` field to `Transaction`.
* Add `customerId` field to `TransactionSearchInput`.
* Add `duplicateOf` field to `GatewayRejectedEvent`. This facilitates safe retries of failed transaction requests.

# 2019-07-11

* Add `defaultPaymentMethod` field to `Customer`.
* Add `tokenizeCustomActionsPaymentMethod` mutation.
* Add `tokenizeUsBankLogin` mutation.
* Add `refunds` search field to `Search` query.
* Add ability to search transactions by status transition time.
* Change `TransactionAmountSearchInput` input name to `MonetaryAmountSearchInput`.
* Deprecate `TransactionStatus#SETTLEMENT_CONFIRMED` enum value. It is no longer applicable to any supported payment method types.

# 2019-06-06

* Add `amount` to `CaptureTransactionInput` to allow you to capture a different amount than the payment method was originally authorized for.
* Change `viewer` query to return `Viewer` type with `user` and `merchant` fields. All top level fields were deprecated in favor of the `User` and `Merchant` objects.
* Add additional input fields on `TransactionInput` to specify shipping, tax, and line items for level 2 and level 3 processing.

# 2019-05-23

* Add `customerId` parameter to `CreateClientTokenInput` to create customer-scoped client tokens.

# 2019-05-17

* Add `deleteCustomer` mutation.
* Add `idFromLegacyId` query.
* Add `legacyId` fields to all types that extend the `Node` interface.
* Add `customerId` to `TransactionInput` to allow associating a transaction with the customer when charging a single-use payment method.
* Add `customer` field on `Transaction`.
* Add `SETTLEMENT_CONFIRMED` to `TransactionStatus` enum.

# 2019-05-03

* Add `updateCustomer` mutation.
* Add nullable `customerId` field to `VaultPaymentMethodInput`.
* The `value` field on `CustomFieldInput` type is now nullable.
* The `achMandate` field on `UsBankAccountInput` type is now non-nullable.

# 2019-04-22

* Add nullable `customer` field to `PaymentMethod`.

# 2019-04-18

* Add `verifyPaymentMethod` mutation.
* Add `createCustomer` mutation.
* Deprecate `ClientConfiguration.ideal`.

# 2019-04-11

* Credit cards are now verified automatically upon vaulting.
* `Verification`s will now be returned on `PaymentMethod`s as a connection.
* The `billingAddress` field on `TokenizeUsBankAccountInput` is now nullable.
* Add `createdAt` parameter to `TransactionSearchInput`.
* The `Node` query now can return `Customer`s and `Verification`s.

# 2019-03-18

* Add `authorizePaymentMethod` and `captureTransaction` mutations.
* Add `channel` field to `TransactionInput` and `Transaction`.
