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
