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
