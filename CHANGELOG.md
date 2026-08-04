# 08-04-2026
* Add new types:
    * `MerchantAccountCapabilities`
* Add new enums:
    * `MerchantAccountType`
* Add new directives:
    * `deprecatedSince`
* Add new enum values:
    * `NARANJA`, `TROY`, `VERVE`, `naranja`, `troy`, `verve` to `CreditCardBrandCode`
    * `MASTER`, `STANDARD`, `SUB_MERCHANT` to `MerchantAccountType`
* Add new fields:
    * `accountType`, `capabilities` to `MerchantAccount`
    * `supportsPublicDescriptors` to `MerchantAccountCapabilities`

# 07-14-2026
* Add new mutations:
    * `deleteRecurringBillingSubscriptionPlanAddOnTemplate`
    * `deleteRecurringBillingSubscriptionPlanDiscountTemplate`
* Add new types:
    * `DeleteRecurringBillingSubscriptionPlanAddOnPayload`
    * `DeleteRecurringBillingSubscriptionPlanDiscountPayload`
* Add new inputs:
    * `DeleteRecurringBillingSubscriptionPlanAddOnTemplateInput`
    * `DeleteRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `SearchACHTypeInput`
* Add new fields:
    * `achType` to `TransactionSearchInput`
    * `clientMutationId` to `DeleteRecurringBillingSubscriptionPlanAddOnPayload`, `DeleteRecurringBillingSubscriptionPlanAddOnTemplateInput`, `DeleteRecurringBillingSubscriptionPlanDiscountPayload`, `DeleteRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `id` to `DeleteRecurringBillingSubscriptionPlanAddOnTemplateInput`, `DeleteRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `in`, `is` to `SearchACHTypeInput`

# 07-07-2026
* Add new mutations:
    * `createRecurringBillingSubscriptionPlanAddOnTemplate`
    * `createRecurringBillingSubscriptionPlanDiscountTemplate`
    * `deleteRecurringBillingSubscriptionPlan`
    * `updateRecurringBillingSubscriptionPlanAddOnTemplate`
    * `updateRecurringBillingSubscriptionPlanDiscountTemplate`
* Add new queries:
    * `businessAccountCreationRequests`
    * `customers`
    * `disputes`
    * `inStoreReaders`
    * `payments`
    * `recurringBillingSubscriptions`
    * `refunds`
    * `roles`
    * `searchInStoreLocations`
    * `transactions`
    * `verifications`
* Add new types:
    * `DeleteRecurringBillingSubscriptionPlanPayload`
    * `RecurringBillingSubscriptionPlanAddOnPayload`
    * `RecurringBillingSubscriptionPlanDiscountPayload`
* Add new inputs:
    * `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`
    * `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `DeleteRecurringBillingSubscriptionPlanInput`
    * `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`
    * `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
* Add new enums:
    * `ThreeDSecurePassThroughNetwork`
* Add new enum values:
    * `EFTPOS`, `MASTERCARD`, `VISA` to `ThreeDSecurePassThroughNetwork`
* Add new fields:
    * `addOn` to `RecurringBillingSubscriptionPlanAddOnPayload`
    * `amount` to `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `clientMutationId` to `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`, `DeleteRecurringBillingSubscriptionPlanInput`, `DeleteRecurringBillingSubscriptionPlanPayload`, `RecurringBillingSubscriptionPlanAddOnPayload`, `RecurringBillingSubscriptionPlanDiscountPayload`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `description` to `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `discount` to `RecurringBillingSubscriptionPlanDiscountPayload`
    * `id` to `DeleteRecurringBillingSubscriptionPlanInput`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `name` to `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
    * `network` to `ThreeDSecurePassThroughInput`
    * `numberOfBillingCycles` to `CreateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `CreateRecurringBillingSubscriptionPlanDiscountTemplateInput`, `UpdateRecurringBillingSubscriptionPlanAddOnTemplateInput`, `UpdateRecurringBillingSubscriptionPlanDiscountTemplateInput`
* Deprecate:
    * `search` on `Query`
    * `businessAccountCreationRequests`, `customers`, `disputes`, `inStoreLocations`, `inStoreReaders`, `payments`, `recurringBillingSubscriptions`, `refunds`, `roles`, `transactions`, `verifications` on `Search`

# 06-30-2026
* Add new mutations:
    * `chargeRecurringBillingSubscription`
* Add new types:
    * `RecurringBillingSubscriptionConnection`
    * `RecurringBillingSubscriptionConnectionEdge`
* Add new inputs:
    * `ChargeRecurringBillingSubscriptionInput`
    * `FraudProtectionCustomFieldInput`
    * `RecurringBillingSubscriptionSearchInput`
* Add new enum values:
    * `DECLINE`, `ERROR` to `ExternalPaymentStatus`
* Add new fields:
    * `amount`, `clientMutationId`, `submitForSettlement`, `subscriptionId` to `ChargeRecurringBillingSubscriptionInput`
    * `billingCyclesRemaining`, `createdAt`, `daysPastDue`, `id`, `inTrialPeriod`, `merchantAccountId`, `nextBillingDate`, `planId`, `price`, `status`, `transactionId` to `RecurringBillingSubscriptionSearchInput`
    * `cursor`, `node` to `RecurringBillingSubscriptionConnectionEdge`
    * `edges`, `pageInfo` to `RecurringBillingSubscriptionConnection`
    * `fallbackUrlScheme` to `PayPalAppSwitchNativeAppInput`
    * `fraudProtectionCustomFields` to `TransactionRiskEvaluateInput`
    * `mastercardTransactionLinkId` to `TransactionAuthorizationProcessorResponse`, `VerificationProcessorResponse`
    * `name`, `value` to `FraudProtectionCustomFieldInput`
    * `readerName` to `PaymentReaderMetadataInput`
    * `recurringBillingSubscriptions` to `Search`
    * `surchargeAmount` to `Transaction`, `TransactionInput`
* Update types:
    * Make `disputeReason` required on `SubmitDisputeFeedbackInput`
    * Make `disputeStatus` required on `SubmitDisputeFeedbackInput`
* Remove deprecation:
    * `selectedFinancingOption` on `PayPalAccountDetails`
* Remove:
    * `AUTHORIZED` from `ExternalPaymentStatus` enum
    * `customFields` field from `TransactionRiskEvaluateInput`
    * `DECLINED` from `ExternalPaymentStatus` enum
    * `FAILED` from `ExternalPaymentStatus` enum
    * `PENDING` from `ExternalPaymentStatus` enum
    * `REFUNDED` from `ExternalPaymentStatus` enum
    * `riskDataId` field from `SubmitDisputeFeedbackInput`
    * `SETTLED` from `ExternalPaymentStatus` enum
    * `TransactionTransferType` type
    * `UNKNOWN` from `ExternalPaymentStatus` enum
    * `VOIDED` from `ExternalPaymentStatus` enum

# 05-19-2026
* Add new mutations:
    * `cancelRecurringBillingSubscription`
    * `createRecurringBillingSubscription`
    * `updateRecurringBillingSubscription`
* Add new types:
    * `RecurringBillingSubscription`
    * `RecurringBillingSubscriptionAddOn`
    * `RecurringBillingSubscriptionDescriptor`
    * `RecurringBillingSubscriptionDiscount`
    * `RecurringBillingSubscriptionPayload`
    * `RecurringBillingSubscriptionStatusEvent`
    * `RecurringBillingSubscriptionTimeline`
* Add new inputs:
    * `CancelRecurringBillingSubscriptionInput`
    * `CreateRecurringBillingSubscriptionInput`
    * `RecurringBillingSubscriptionAddOnInput`
    * `RecurringBillingSubscriptionDescriptorInput`
    * `RecurringBillingSubscriptionDiscountInput`
    * `RecurringBillingSubscriptionModificationInput`
    * `RecurringBillingSubscriptionOptionsInput`
    * `RecurringBillingSubscriptionReplaceExistingModificationsInput`
    * `RecurringBillingSubscriptionRetainExistingAddOnsInput`
    * `RecurringBillingSubscriptionRetainExistingDiscountsInput`
    * `RecurringBillingSubscriptionRetainExistingModificationsInput`
    * `RecurringBillingSubscriptionStartDateInput`
    * `UpdateRecurringBillingSubscriptionInput`
    * `UpdateRecurringBillingSubscriptionOptionsInput`
* Add new enums:
    * `RecurringBillingSubscriptionSource`
    * `RecurringBillingSubscriptionStatus`
* Add new enum values:
    * `RECURRING_BILLING_SUBSCRIPTION` to `LegacyIdType`
    * `API`, `CONTROL_PANEL`, `RECURRING` to `RecurringBillingSubscriptionSource`
    * `ACTIVE`, `CANCELED`, `EXPIRED`, `PAST_DUE`, `PENDING` to `RecurringBillingSubscriptionStatus`
* Add new fields:
    * `add` to `RecurringBillingSubscriptionRetainExistingAddOnsInput`, `RecurringBillingSubscriptionRetainExistingDiscountsInput`
    * `addOnId` to `RecurringBillingSubscriptionAddOn`, `RecurringBillingSubscriptionAddOnInput`
    * `addOns` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionReplaceExistingModificationsInput`, `RecurringBillingSubscriptionRetainExistingModificationsInput`
    * `amount` to `RecurringBillingSubscriptionAddOn`, `RecurringBillingSubscriptionAddOnInput`, `RecurringBillingSubscriptionDiscount`, `RecurringBillingSubscriptionDiscountInput`
    * `balance` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionStatusEvent`
    * `billingDayOfMonth` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionStartDateInput`
    * `billingPeriodEndDate`, `billingPeriodStartDate`, `createdAt`, `nextBillingDate`, `paidThroughDate`, `updatedAt` to `RecurringBillingSubscriptionTimeline`
    * `cancelAppUrl`, `returnAppUrl` to `PayPalAppSwitchNativeAppInput`
    * `clientMutationId` to `CancelRecurringBillingSubscriptionInput`, `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscriptionPayload`, `UpdateRecurringBillingSubscriptionInput`
    * `companyName` to `RecurringBillingSubscriptionDescriptor`, `RecurringBillingSubscriptionDescriptorInput`
    * `currencyIsoCode`, `subscriptionSource`, `timestamp` to `RecurringBillingSubscriptionStatusEvent`
    * `currentBillingCycle` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionAddOn`, `RecurringBillingSubscriptionDiscount`
    * `daysPastDue`, `failureCount`, `id`, `legacyId`, `nextBillingPeriodAmount`, `statusHistory`, `timeline`, `transactionIds` to `RecurringBillingSubscription`
    * `descriptor` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `UpdateRecurringBillingSubscriptionInput`
    * `discountId` to `RecurringBillingSubscriptionDiscount`, `RecurringBillingSubscriptionDiscountInput`
    * `discounts` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionReplaceExistingModificationsInput`, `RecurringBillingSubscriptionRetainExistingModificationsInput`
    * `edit` to `RecurringBillingSubscriptionRetainExistingAddOnsInput`, `RecurringBillingSubscriptionRetainExistingDiscountsInput`
    * `firstBillingDate` to `RecurringBillingSubscriptionStartDateInput`, `RecurringBillingSubscriptionTimeline`
    * `merchantAccountId` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `UpdateRecurringBillingSubscriptionInput`
    * `modifications` to `CreateRecurringBillingSubscriptionInput`, `UpdateRecurringBillingSubscriptionInput`
    * `numberOfBillingCycles` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `RecurringBillingSubscriptionAddOn`, `RecurringBillingSubscriptionAddOnInput`, `RecurringBillingSubscriptionDiscount`, `RecurringBillingSubscriptionDiscountInput`, `UpdateRecurringBillingSubscriptionInput`
    * `options` to `CreateRecurringBillingSubscriptionInput`
    * `overrides` to `UpdateRecurringBillingSubscriptionInput`
    * `paymentMethodId` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `UpdateRecurringBillingSubscriptionInput`
    * `payPalDescription` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `UpdateRecurringBillingSubscriptionInput`
    * `phoneNumber` to `RecurringBillingSubscriptionDescriptor`, `RecurringBillingSubscriptionDescriptorInput`
    * `planId` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `RecurringBillingSubscriptionStatusEvent`, `UpdateRecurringBillingSubscriptionInput`
    * `price` to `CreateRecurringBillingSubscriptionInput`, `RecurringBillingSubscription`, `RecurringBillingSubscriptionStatusEvent`, `UpdateRecurringBillingSubscriptionInput`
    * `prorateCharges`, `revertSubscriptionOnProrationFailure` to `UpdateRecurringBillingSubscriptionOptionsInput`
    * `quantity` to `RecurringBillingSubscriptionAddOn`, `RecurringBillingSubscriptionAddOnInput`, `RecurringBillingSubscriptionDiscount`, `RecurringBillingSubscriptionDiscountInput`
    * `remove` to `RecurringBillingSubscriptionRetainExistingAddOnsInput`, `RecurringBillingSubscriptionRetainExistingDiscountsInput`
    * `replaceExisting`, `retainExisting` to `RecurringBillingSubscriptionModificationInput`
    * `startDate`, `startImmediately` to `RecurringBillingSubscriptionOptionsInput`
    * `status` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionStatusEvent`
    * `subscription` to `RecurringBillingSubscriptionPayload`
    * `subscriptionId` to `CancelRecurringBillingSubscriptionInput`, `UpdateRecurringBillingSubscriptionInput`
    * `trial` to `RecurringBillingSubscription`, `RecurringBillingSubscriptionStartDateInput`
    * `url` to `RecurringBillingSubscriptionDescriptor`, `RecurringBillingSubscriptionDescriptorInput`
* Add interface implementations:
    * `RecurringBillingSubscription` now implements `Node`
* Remove:
    * `appUrl` field from `PayPalAppSwitchNativeAppInput`

# 04-30-2026
* Add new mutations:
    * `createBillingAgreementJwt`
* Add new queries:
    * `idsFromLegacyIds`
* Add new types:
    * `CreateBillingAgreementJwtPayload`
* Add new inputs:
    * `CreateBillingAgreementJwtInput`
    * `IdsFromLegacyIdsInput`
    * `LegacyIdElementsInput`
* Add new fields:
    * `clientMutationId` to `CreateBillingAgreementJwtInput`, `CreateBillingAgreementJwtPayload`
    * `ids` to `IdsFromLegacyIdsInput`
    * `jwt` to `CreateBillingAgreementJwtPayload`
    * `legacyId`, `type` to `LegacyIdElementsInput`
    * `paymentMethodId` to `ClientTokenInput`
    * `paymentMethodJwt` to `CreateBillingAgreementJwtInput`
* Deprecate:
    * `idFromLegacyId` on `Query`
* Remove:
    * `fundingInstrumentDetails` field from `VenmoAccountDetails`
    * `VenmoFundingInstrumentDetails` type
    * `VenmoPrimaryFundingInstrumentType` type
    * `VenmoSecondaryFundingInstrumentType` type

# 04-20-2026
* Add new mutations:
    * `createRecurringBillingSubscriptionPlan`
    * `submitDisputeFeedback`
    * `submitTransactionFeedback`
    * `updateRecurringBillingSubscriptionPlan`
* Add new queries:
    * `recurringBillingSubscriptionPlanAddOns`
    * `recurringBillingSubscriptionPlanDiscounts`
    * `recurringBillingSubscriptionPlans`
* Add new types:
    * `RecurringBillingSubscriptionPlan`
    * `RecurringBillingSubscriptionPlanAddOn`
    * `RecurringBillingSubscriptionPlanAddOnsPayload`
    * `RecurringBillingSubscriptionPlanDiscount`
    * `RecurringBillingSubscriptionPlanDiscountsPayload`
    * `RecurringBillingSubscriptionPlanPayload`
    * `RecurringBillingSubscriptionPlansPayload`
    * `RecurringBillingSubscriptionTrial`
    * `SubmitFeedbackPayload`
    * `VenmoFundingInstrumentDetails`
* Add new inputs:
    * `CreateRecurringBillingSubscriptionPlanAddOnInput`
    * `CreateRecurringBillingSubscriptionPlanDiscountInput`
    * `CreateRecurringBillingSubscriptionPlanInput`
    * `ExternalPaymentResponseInput`
    * `ExternalProcessorResponseInput`
    * `RecurringBillingSubscriptionTrialInput`
    * `SubmitDisputeFeedbackInput`
    * `SubmitTransactionFeedbackInput`
    * `UpdateRecurringBillingSubscriptionPlanAddOnInput`
    * `UpdateRecurringBillingSubscriptionPlanDiscountInput`
    * `UpdateRecurringBillingSubscriptionPlanInput`
* Add new enums:
    * `ExternalPaymentStatus`
    * `RecurringBillingSubscriptionTrialDurationUnit`
    * `UpdateModificationOperation`
    * `VenmoPrimaryFundingInstrumentType`
    * `VenmoSecondaryFundingInstrumentType`
* Add new enum values:
    * `AUTHORIZED`, `DECLINED`, `FAILED`, `PENDING`, `REFUNDED`, `REJECTED`, `SETTLED`, `SUCCESS`, `UNKNOWN`, `VOIDED` to `ExternalPaymentStatus`
    * `RECURRING_BILLING_SUBSCRIPTION_PLAN`, `RECURRING_BILLING_SUBSCRIPTION_PLAN_ADD_ON`, `RECURRING_BILLING_SUBSCRIPTION_PLAN_DISCOUNT` to `LegacyIdType`
    * `BIZUM`, `KLARNA`, `SKRILL`, `TWINT` to `LocalPaymentMethodType`
    * `BIZUM_VIA_PAYPAL`, `KLARNA_VIA_PAYPAL`, `SKRILL_VIA_PAYPAL`, `TWINT_VIA_PAYPAL` to `PaymentMethodSnapshotSearchType`
    * `DAY`, `MONTH` to `RecurringBillingSubscriptionTrialDurationUnit`
    * `PERSON_TO_PERSON_BANK_INITIATED`, `PREPAID_TOP_UP` to `TransactionTransferType`
    * `ADD`, `EDIT`, `REMOVE` to `UpdateModificationOperation`
    * `BALANCE`, `BANK`, `CREDIT`, `DEBIT` to `VenmoPrimaryFundingInstrumentType`
    * `BANK`, `CREDIT`, `DEBIT` to `VenmoSecondaryFundingInstrumentType`
* Add new fields:
    * `action` to `UpdateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`
    * `addOnId` to `CreateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanAddOnInput`
    * `addOns` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOnsPayload`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `amount` to `CreateRecurringBillingSubscriptionPlanAddOnInput`, `CreateRecurringBillingSubscriptionPlanDiscountInput`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`, `UpdateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`
    * `amountDisputed`, `disputeCreatedAt`, `disputeReason`, `disputeStatus` to `SubmitDisputeFeedbackInput`
    * `avsResponseCode`, `cvvResponseCode` to `ExternalProcessorResponseInput`
    * `billingDayOfMonth` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `billingFrequency` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `clientMutationId` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlanPayload`, `SubmitDisputeFeedbackInput`, `SubmitFeedbackPayload`, `SubmitTransactionFeedbackInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `countryName` to `Merchant`
    * `createdAt` to `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`
    * `currentBalance`, `primaryFILast4`, `primaryFIType`, `secondaryFILast4`, `secondaryFIType` to `VenmoFundingInstrumentDetails`
    * `description` to `CreateRecurringBillingSubscriptionPlanAddOnInput`, `CreateRecurringBillingSubscriptionPlanDiscountInput`, `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`, `UpdateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `discountId` to `CreateRecurringBillingSubscriptionPlanDiscountInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`
    * `discounts` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanDiscountsPayload`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `duration` to `RecurringBillingSubscriptionTrial`, `RecurringBillingSubscriptionTrialInput`
    * `durationUnit` to `RecurringBillingSubscriptionTrial`, `RecurringBillingSubscriptionTrialInput`
    * `externalPaymentResponse`, `externalProcessorResponse` to `SubmitTransactionFeedbackInput`
    * `externalTransactionId` to `SubmitDisputeFeedbackInput`, `SubmitTransactionFeedbackInput`
    * `fundingInstrumentDetails` to `VenmoAccountDetails`
    * `id` to `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `legacyId` to `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`
    * `modificationIds` to `CreateRecurringBillingSubscriptionPlanInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `monetaryAmount` to `CreateRecurringBillingSubscriptionPlanInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `name` to `CreateRecurringBillingSubscriptionPlanAddOnInput`, `CreateRecurringBillingSubscriptionPlanDiscountInput`, `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`, `UpdateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `numberOfBillingCycles` to `CreateRecurringBillingSubscriptionPlanAddOnInput`, `CreateRecurringBillingSubscriptionPlanDiscountInput`, `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`, `UpdateRecurringBillingSubscriptionPlanAddOnInput`, `UpdateRecurringBillingSubscriptionPlanDiscountInput`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `plan` to `RecurringBillingSubscriptionPlanPayload`
    * `plans` to `RecurringBillingSubscriptionPlansPayload`
    * `price` to `RecurringBillingSubscriptionPlan`
    * `readerId` to `CardPresentOriginDetails`, `EmvCardOriginDetails`, `InStoreReaderOriginDetails`, `PaymentSearchInput`, `RefundSearchInput`, `TransactionSearchInput`
    * `reason`, `status` to `ExternalPaymentResponseInput`
    * `riskDataId` to `SubmitDisputeFeedbackInput`, `SubmitTransactionFeedbackInput`
    * `storeId` to `CardPresentOriginDetails`, `EmvCardOriginDetails`, `InStoreReaderOriginDetails`
    * `trial` to `CreateRecurringBillingSubscriptionPlanInput`, `RecurringBillingSubscriptionPlan`, `UpdateRecurringBillingSubscriptionPlanInput`
    * `updatedAt` to `RecurringBillingSubscriptionPlan`, `RecurringBillingSubscriptionPlanAddOn`, `RecurringBillingSubscriptionPlanDiscount`
* Add interface implementations:
    * `RecurringBillingSubscriptionPlan` now implements `Node`
    * `RecurringBillingSubscriptionPlanAddOn` now implements `Node`
    * `RecurringBillingSubscriptionPlanDiscount` now implements `Node`
* Remove:
    * `PREPAID_TOPUP` from `TransactionTransferType` enum
    * `surchargeAmount` field from `Transaction`
    * `surchargeAmount` field from `TransactionInput`

# 02-17-2026
* Add new types:
    * `UsBankAccountTransactionDetails`
* Add new enums:
    * `ACHType`
* Add new enum values:
    * `SAME_DAY`, `STANDARD` to `ACHType`
* Add new fields:
    * `achType` to `ChargeUsBankAccountInput`, `UsBankAccountTransactionDetails`
    * `requestedAchType`, `usBankAccount` to `UsBankAccountTransactionDetails`
* Remove:
    * `Duration` type
    * `PayPalFinancingCreditProductIdentifier` type
    * `PayPalFinancingOption` type
    * `PayPalFinancingOptionCreditType` type
    * `paypalFinancingOptions` query
    * `PayPalFinancingOptionsInput` type
    * `PayPalFinancingOptionsPayload` type
    * `PayPalQualifyingFinancingOption` type

# 02-11-2026
* Add new mutations:
    * `createLocalPaymentContext`
    * `evaluateTransactionRisk`
    * `updatePayPalOneTimePayment`
* Add new types:
    * `CreateLocalPaymentContextPayload`
    * `RoleConnectionEdge`
    * `RoleSearchConnection`
    * `TransactionRiskEvaluatePayload`
    * `UpdatePayPalOneTimePaymentPayload`
* Add new inputs:
    * `CreateLocalPaymentContextInput`
    * `CreditCardDetachedRefundOptionsInput`
    * `EvaluateTransactionRiskInput`
    * `LocalPaymentContextInput`
    * `RoleSearchInput`
    * `TransactionRiskEvaluateInput`
    * `UpdatePayPalOneTimePaymentInput`
* Add new enums:
    * `ExternalProcessor`
* Add new enum values:
    * `ADYEN`, `AMAZON_PAY`, `AUTHORIZE_NET`, `CHASE`, `FISERV`, `NUVEI`, `SQUARE`, `STRIPE`, `WORLDPAY` to `ExternalProcessor`
    * `FRAUD_PROTECTION_EXTERNAL` to `FraudServiceProvider`
    * `CRYPTO` to `LocalPaymentMethodType`
    * `CRYPTO_VIA_PAYPAL` to `PaymentMethodSnapshotSearchType`
* Add new fields:
    * `achRejectReason`, `achReturnCode` to `TransactionSettlementProcessorResponse`
    * `amount` to `LocalPaymentContextInput`, `TransactionRiskEvaluateInput`, `UpdatePayPalOneTimePaymentInput`
    * `amountBreakdown`, `customField`, `description`, `payeeEmail`, `shippingOptions` to `UpdatePayPalOneTimePaymentInput`
    * `billingAddress`, `customFields`, `customerDetails`, `customerId`, `externalProcessor`, `paymentInitiator` to `TransactionRiskEvaluateInput`
    * `cancelUrl`, `countryCode`, `expiryDate`, `locale`, `merchantAccountId`, `payerInfo`, `returnUrl`, `type` to `LocalPaymentContextInput`
    * `clientMutationId` to `CreateLocalPaymentContextInput`, `CreateLocalPaymentContextPayload`, `EvaluateTransactionRiskInput`, `TransactionRiskEvaluatePayload`, `UpdatePayPalOneTimePaymentInput`, `UpdatePayPalOneTimePaymentPayload`
    * `cursor`, `node` to `RoleConnectionEdge`
    * `edges`, `pageInfo` to `RoleSearchConnection`
    * `failOnDuplicatePaymentMethodForCustomer` to `ClientTokenInput`
    * `id` to `RoleSearchInput`
    * `lineItems` to `TransactionRiskEvaluateInput`, `UpdatePayPalOneTimePaymentInput`
    * `merchantCategoryCode` to `CreditCardDetachedRefundOptionsInput`, `InStoreCreditCardRefundOptionsInput`
    * `offerPayPalCredit` to `CreatePayPalOneTimePaymentInput`
    * `options` to `RefundCreditCardInput`
    * `orderId` to `LocalPaymentContextInput`, `TransactionRiskEvaluateInput`, `UpdatePayPalOneTimePaymentInput`
    * `paymentContext` to `CreateLocalPaymentContextInput`, `CreateLocalPaymentContextPayload`
    * `paymentMethod` to `UpdatePayPalOneTimePaymentPayload`
    * `paymentMethodId` to `EvaluateTransactionRiskInput`, `UpdatePayPalOneTimePaymentInput`
    * `phoneCountryCode` to `LocalPaymentPayerInfoInput`
    * `processorSettlementResponse` to `Transaction`
    * `riskData` to `TransactionRiskEvaluateInput`, `TransactionRiskEvaluatePayload`
    * `roles` to `Search`
    * `shippingAddress` to `TransactionRiskEvaluateInput`, `UpdatePayPalOneTimePaymentInput`
    * `transaction` to `EvaluateTransactionRiskInput`
    * `venmoRiskCorrelationId` to `CreateVenmoPaymentContextInput`, `VenmoPaymentContext`
* Deprecate:
    * `visaCheckout` on `ClientConfiguration`
    * `VISA_CHECKOUT` on `PaymentMethodOriginType`
    * `CREDIT_CARD_VIA_VISA_CHECKOUT` on `PaymentMethodSnapshotSearchType`
    * `LOOKUP_ENROLLED` on `ThreeDSecureAuthenticationStatus`
    * `achRejectReason`, `achReturnCode` on `UsBankAccountDetails`

# 11-18-2025
* Add new mutations:
    * `voidTransaction`
* Add new types:
    * `VenmoAppSwitchContext`
    * `VenmoAppSwitchMobileWeb`
    * `VoidTransactionPayload`
* Add new inputs:
    * `VenmoAppSwitchContextInput`
    * `VenmoAppSwitchMobileWebInput`
    * `VoidTransactionInput`
* Add new enum values:
    * `FUND_DISBURSEMENT`, `PAYROLL_DISBURSEMENT`, `PREPAID_TOPUP` to `TransactionTransferType`
* Add new fields:
    * `apiRequestKey`, `transactionId` to `VoidTransactionInput`
    * `appSwitchContext` to `CreateVenmoPaymentContextInput`, `VenmoPaymentContext`
    * `buyerUserAgent` to `VenmoAppSwitchMobileWeb`, `VenmoAppSwitchMobileWebInput`
    * `clientMutationId` to `VoidTransactionInput`, `VoidTransactionPayload`
    * `isIncognito` to `VenmoAppSwitchMobileWeb`, `VenmoAppSwitchMobileWebInput`
    * `merchantCategoryCode` to `TransactionInput`
    * `merchantId`, `processorResponse` to `Refund`
    * `mobileWeb` to `VenmoAppSwitchContext`, `VenmoAppSwitchContextInput`
    * `paymentAccountReference` to `ApplePayOriginDetails`, `CreditCardDetails`, `GooglePayOriginDetails`
    * `processorAuthorizationResponse` to `Refund`, `Transaction`
    * `transaction` to `VoidTransactionPayload`
* Deprecate:
    * `selectedFinancingOption` on `PayPalAccountDetails`
    * `selectedFinancingOption` on `PayPalTransactionDetails`
    * `paypalFinancingOptions` on `Query`
    * `processorResponse` on `Refund`
* Remove:
    * `amount` field from `CaptureTransactionInput`
    * `ApplicationBankAccountPurpose` type
    * `ApplicationStatus` type
    * `authenticationResponse` field from `ThreeDSecurePassThroughInput`
    * `chargebackProtectionLevel` field from `DisputeSearchInput`
    * `countryCodeAlpha2` field from `AddressInput`
    * `countryCodeAlpha3` field from `AddressInput`
    * `countryCodeNumeric` field from `AddressInput`
    * `countryName` field from `AddressInput`
    * `createProductRequestForMerchant` mutation
    * `CreateProductRequestForMerchantInput` type
    * `currencyIsoCode` field from `MonetaryAmountSearchInput`
    * `disableProductForMerchant` mutation
    * `DisableProductForMerchantInput` type
    * `DisableProductForMerchantPayload` type
    * `email` field from `SearchPaymentPayPalDetailsInput`
    * `enableProductForMerchant` mutation
    * `EnableProductForMerchantInput` type
    * `EnableProductForMerchantPayload` type
    * `MerchantAccountApplication` type
    * `merchantAccountId` field from `CreditCardVerificationOptionsInput`
    * `MVVAcceptanceChannel` type
    * `MVVRegistrationType` type
    * `MVVUtilityType` type
    * `OwnerAddressType` type
    * `OwnerIDType` type
    * `OwnerPhoneType` type
    * `OwnerPosition` type
    * `OwnerRole` type
    * `payee` field from `AuthorizePayPalAccountOptionsInput`
    * `payee` field from `ChargePayPalAccountOptionsInput`
    * `Product` type
    * `ProductCode` type
    * `ProductEnablementStatus` type
    * `ProductRequestPayload` type
    * `products` field from `Merchant`
    * `ProductsInput` type
    * `reason` field from `RefundInput`
    * `recurring` field from `TransactionInput`
    * `RefundPolicy` type
    * `selectedFinancingOption` field from `ChargePayPalAccountOptionsInput`
    * `threeDSecurePassThrough` field from `TransactionInput`
    * `userAgent` field from `ThreeDSecureLookupTransactionInformationInput`
    * `verificationMerchantAccountId` field from `VaultPaymentMethodInput`

# 10-14-2025
* Add new field
    * `apiRequestKey` to `AuthorizeCreditCardInput`
    * `apiRequestKey` to `AuthorizeInStoreCreditCardInput`
    * `apiRequestKey` to `AuthorizePaymentMethodInput`
    * `apiRequestKey` to `AuthorizePayPalAccountInput`
    * `apiRequestKey` to `AuthorizeVenmoAccountInput`
    * `apiRequestKey` to `CaptureTransactionInput`
    * `apiRequestKey` to `ChargeCreditCardInput`
    * `apiRequestKey` to `ChargeInStoreCreditCardInput`
    * `apiRequestKey` to `ChargePaymentMethodInput`
    * `apiRequestKey` to `ChargePayPalAccountInput`
    * `apiRequestKey` to `ChargeUsBankAccountInput`
    * `apiRequestKey` to `ChargeVenmoAccountInput`
    * `apiRequestKey` to `PartialCaptureTransactionInput`
    * `apiRequestKey` to `RefundCreditCardInput`
    * `apiRequestKey` to `RefundInStoreCreditCardInput`
    * `apiRequestKey` to `RefundTransactionInput`
    * `apiRequestKey` to `RefundUsBankAccountInput`
* Update enum value
    * `INSTANT_VERIFICATION` to `INSTANT_VERIFICATION_ACCOUNT_VALIDATION` in `UsBankAccountVerificationMethod`

# 09-18-2025
* New mutation: 
    * `registerApplePayDomains`
* New query: 
    * `applePayRegisteredDomains`
* New types: 
    * `OpenBankingConfiguration`
    * `RegisterApplePayDomainsPayload`
    * `ApplePayRegisteredDomainsPayload`
* New input type:
    * `RegisterApplePayDomainsInput`

# 08-12-2025
* Add new enum
    * `AccountInformationInquiry`
    * `PayPalAppSwitchOsType`
    * `PayPalAppSwitchReturnFlow`
    * `PayPalBillingAgreementExperienceStatus`
    * `PayPalBillingAgreementUserAction`
    * `PayPalOrderExperienceStatus`
    * `PayPalOrderStatus`
    * `ProductEnablementStatus` values `DISABLING`, `ENABLING`
    * `TransactionTransferType`
* Add new input
    * `AuthorizeInStoreCreditCardInput`
    * `ChargeInStoreCreditCardInput`
    * `CreateOfflineDeclinedTransactionInput`
    * `CreateTransactionRiskContextInput`
    * `EmvCardInput`
    * `InStoreCreditCardRefundOptionsInput`
    * `InStoreCreditCardTransactionOptionsInput`
    * `MagstripeCardInput`
    * `PaymentFacilitatorInput`
    * `PaymentReaderMetadataInput`
    * `PayPalAmountBreakDownInput`
    * `PayPalAppSwitchContextInput`
    * `PayPalAppSwitchMobileWebInput`
    * `PayPalAppSwitchNativeAppInput`
    * `PayPalOrderDetailsInput`
    * `PayPalTransactionRiskContextDataFieldInput`
    * `PayPalTransactionRiskContextInput`
    * `RefundInStoreCreditCardInput`
    * `ReverseEmvTransactionInput`
    * `SubMerchantDetailsInput`
    * `TokenizeEmvCardInput`
    * `TokenizeMagstripeCardInput`
    * `UpdateEmvCaptureDataInput`
* Add new type
    * `PayPalOrderDetailsPayload`
    * `TokenizeEmvCardPayload`
    * `TokenizeMagstripeCardPayload`
    * `TransactionRiskContextPayload`
* Add new mutation
    * `authorizeInStoreCreditCard`
    * `chargeInStoreCreditCard`
    * `createOfflineDeclinedTransaction`
    * `createTransactionRiskContext`
    * `refundInStoreCreditCard`
    * `reverseEmvTransaction`
    * `tokenizeEmvCard`
    * `tokenizeMagstripeCard`
    * `updateEmvCaptureData`
* Add new query
    * `paypalOrderDetails`
* Add new field
    * `business`, `consumer`, `corporate`, `purchase` to `BinRecord`
    * `achMandate`, `achMandateAcceptedAt` to `ChargeUsBankAccountInput`
    * `appSwitchContext`, `amountBreakDown`, `recurringBillingPlan` to `CreatePayPalOneTimePaymentInput`
    * `appSwitchContext` to `CreatePayPalBillingAgreementInput`
    * `launchPayPalApp` to `CreatePayPalBillingAgreementPayload`, `CreatePayPalOneTimePaymentPayload`
    * `experienceStatus` to `PayPalBillingAgreementDetailsPayload`
    * `remainingFileEvidenceStorage` to `Dispute`
    * `userAction` to `PayPalBillingAgreementExperienceProfileInput`
    * `statusDetails` to `Product`
    * `upcomingRetryDate` to `Transaction`
    * `cardinalSongbirdUrl`, `cardinalSongbirdIdentityHash` to `ThreeDSecureConfiguration`
    * `acceptPartialAuthorization`, `paymentFacilitator` to `TransactionInput`
    * `achMandate`, `achMandateAcceptedAt` to `VaultUsBankAccountInput`
* Add new enum value
    * `ESTIMATED_MOTO` to `PaymentInitiator`
    * `NETWORK_TOKENS`, `SMART_RETRIES` to `ProductCode`
* Remove
    * `CreateCustomerSessionInput` input
    * `CustomerRecommendations` union
    * `CustomerRecommendationsInput` input
    * `CustomerRecommendationsPayload` type
    * `CustomerSessionInput` input
    * `CustomerSessionPayload` type
    * `PaymentOptions` type
    * `PaymentRecommendations` type
    * `RecommendationPaymentOption` enum
    * `Recommendations` enum
    * `UpdateCustomerSessionInput` input
    * `createCustomerSession` mutation
    * `updateCustomerSession` mutation
    * `customerRecommendations` query
    * `MANUAL_KEY_ENTRY` from `PaymentReaderInputMode` enum
* Update type
    * Make `cryptogram` nullable on `NetworkTokenInput`
    * Change `quantity` from `Float` to `Int` on `PayPalRecurringBillingProductInput`
* Deprecate
    * `acceptanceText` on `UsBankAccountAchMandate`
    * `authenticationResponse` on `ThreeDSecurePassThroughInput`
    * `clientMetadataId` on `TransactionRiskContextPayload`

# 04-29-2025
* Add new field
    * `returnUrl` to `TokenizePayPalBillingAgreementPayload`

# 04-15-2025
* Add new input
    * `PayPalBillingAgreementDetailsInput`
* Add new type
    * `PayPalBillingAgreementDetailsPayload`
* Add new enum
    * `PayPalBillingAgreementStatus`
* Add new query
    * `paypalBillingAgreementDetails`
 
# 04-03-2025
* Add new directive
    * `oneOf`
* Add new field
    * `merchantTokenIdentifier` on `ApplePayOriginDetails`
    * `prepaidReloadable` on `BinRecord`
    * `customerSessionId` on `CreatePayPalBillingAgreementInput`, `CreatePayPalOneTimePaymentInput`
    * `tokensOnDemand` on `FastlaneConfiguration`
    * `fundingSourceDescription`, `vaultedBillingAgreementId` on `PayPalAccountDetails`
    * `contactPreference` on `PayPalExperienceProfileInput`
* Add new input
    * `GenerateEditFundingInstrumentUrlInput`
* Add new type
    * `TokenExchangeConfiguration`
    * `TokensOnDemandConfiguration`
    * `GenerateEditFundingInstrumentUrlPayload`
* Add new mutation
    * `generateEditFundingInstrumentUrl`
* Add new enum
    * `PayPalUserContactPreference`
* Add new enum value
    * `SKIPPED_DUE_TO_ADAPTIVE_AUTHENTICATION` on `ThreeDSecureAuthenticationStatus`

# 02-12-2025
* Add new field
    * `phone` to `Address`, `AddressInput`
    * `recurringBillingPlan` to `CreatePayPalBillingAgreementInput`
    * `payerEmail` to `CreatePayPalOneTimePaymentInput`
    * `recipientEmail` to `EmailAddress`
    * `shippingCallbackUrl` to `CreatePayPalOneTimePaymentInput`
    * `blikAliases` on `PayPalLocalPaymentOriginDetails`
    * `recipientEmail`, `recipientPhone` on `PayPalTransactionDetails`
    * `achReturnCode` on `UsBankAccountDetails`
    * `failOnDuplicatePaymentMethodForCustomer` on `VaultCreditCardInput`
* Add new query
    * `customerRecommendations`
* Deprecate
    * `phoneNumber` on `Address`
    * `samsungPay` on `ClientConfiguration
    * `BOLETOBANCARIO` value on `LocalPaymentMethodType`, `NonInstantLocalPaymentMethodType`
    * `tokenizeSamsungPayCard` mutation
    * `TokenizeSamsungPayCardInput` input
    * `TokenizeSamsungPayCardPayload` type
    * `SamsungPayCardDetails` type
    * `SamsungPayConfiguration` type
    * `SamsungPayOriginDetails` type
    * `SamsungPayEnviornment` enum
    * `SamsungPayCardInput` input
    * `SAMSUNG_PAY` on `PaymentMethodOriginType`
    * `CREDIT_CARD_VIA_SAMSUNG_PAY`, `BOLETOBANCARIO_VIA_PAYPAL` on `PaymentMethodSnapshotSearchType`
* Add new input
    * `CreateCustomerSessionInput`
    * `CustomerRecommendationsInput`
    * `CustomerSessionInput`
    * `PayPalRecurringBillingCycleInput`
    * `PayPalRecurringBillingFrequencyIntervalInput`
    * `PayPalRecurringBillingOneTimeChargesInput`
    * `PayPalRecurringBillingPlanInput`
    * `PayPalRecurringBillingPlanMetadataInput`
    * `PayPalRecurringBillingPricingSchemeInput`
    * `PayPalRecurringBillingProductInput`
    * `UpdateCustomerSessionInput`
* Add new union
    * `CustomerRecommendations`
* Add new type
    * `CustomerRecommendationsPayload`
    * `CustomerSessionPayload`
    * `LocalPaymentBlikAlias`
    * `PaymentOptions`
    * `PaymentRecomendations`
    * `Phone`
* Add new enum
    * `FrequencyUnit`
    * `PayPalRecurringBillingPlan`
    * `PayPalRecurringBillingPricingModel`
    * `RecommendationPaymentOption`
    * `Recommendations`
* Add new enum value
    * `DELAYED_SHIPMENT`, `PAYMENT_WITH_MULTIPLE_MERCHANTS`, `SPLIT_SHIPMENT` on `ThreeDSecureAuthenticationTransactionType`
    * `BANCOMATPAY`, `MBWAY` to `LocalPaymentMethodType`,
    * `BANCOMATPAY_VIA_PAYPAL`, `MBWAY_VIA_PAYPAL` to `PaymentMethodSnapshotSearchType`
* Add new mutation
    * `createCustomerSession`
    * `updateCustomerSession`
* Remove
    * `CreateInStoreFirmwareUpdateScheduleInput`
    * `CreateUnStoreFirmwareUpdateSchedulePayload`
    * `email` field from `CreatePayPalOneTimePaymentInput`
    * `InStoreFirmwareUpdateSchedule`
    * `geoCoordinates` field from `InStoreLocationInput`, `InStoreLocationUpdateInput`
    * `locationId`, `softwareVersion`, `readerStatus` fields from `InStoreReaderPayload`
    * `taxInfo` field from `LocalPaymentPayerInfoInput`
    * `createInStoreFirmwareUpdateSchedule` mutation
    * `TaxInfoInput` input
    * `merchantAccountId` field from `UpdateCreditcardBillingAddressInput`, `VerifyCreditCardInput`
    * `lineItems` field from `VenmoPaysheetTransactionDetailsInput`

# 08-27-2024
* Add new enum 
    * `AniNameResponseCode`
    * `InStorePrintAlignment`
    * `InStorePrintTextDecoration`
    * `InStorePrintTextFontStyle`
    * `InStorePrintTextFontWeight`
    * `ThreeDSecurePriorAuthenticationMethod`
* Add new input
    * `CreateDisputeTextEvidencePayload`
    * `CreateInStoreFirmwareUpdateScheduleInput
    * `CreateOAuthClientSecretInput`
    * `CreateProductRequestForMerchantInput`
    * `DeleteOAuthClientSecretInput`
    * `DisableOAuthClientSecretInput`
    * `InStorePrintContentInput`
    * `InStorePrintImageInput` 
    * `InStorePrintTextInput`
    * `InStoreReaderConditionInput`
    * `RequestPrintFromInStoreReaderInput`
    * `ThreeDSecurePriorAuthenticationDetailsInput`
* Add new type
    * `CreateInStoreFirmwareUpdateSchedulePayload`
    * `CreateOAuthClientSecretPayload`
    * `DeleteOAuthClientSecretPayload`
    * `DisableOauthClientSecretPayload`
    * `InStoreFirmwareUpdateSchedule`
    * `OAuthClientSecret`
    * `ProductRequestPayload`
    * `RequestPrintInStoreContext`
* Add new field
    * `conditionsIn` on `InStoreReaderConditionInput`
    * `finalCapture` on `PartialCaptureTransactionOptionsInput`
    * `shippingTaxAmount` on `TransactionShipping`, `TransactionShippingInput`
* Add new mutation
    * `createInStoreFirmwareUpdateSchedule`
    * `requestPrintFromInStoreReader`
    * `createOAuthClientSecret`
    * `disableOAuthClientSecret`
    * `deleteOAuthClientSecret`
    * `createProductRequestForMerchant`
* Conditional change
    * Make `conditionsIn` field of `InStoreLocationSearchInput` no longer required 

# 07-15-2024
* Add new input
    * `DeleteInStoreLocationInput`
* Add new type
    * `DeleteInStoreLocationPayload`
* Update doc strings
    * Fields in `InStoreLocationAddressSearchInput` and `InStoreLocationConditionInput` of `SearchTextValueInput` type to clarify case-insensitivity
    * Change `creating` to `updating` for `UpdateInStoreLocationPayload`
* Change `geoCoordinates` field in `InStoreLocationInput` to no longer be required
* Add new mutation
    * `deleteInStoreLocation`
* Add new enum value
    * `ADD_SURCHARGE_MID` and `IN_PERSON` to `ProductCode`
    * `PAYMENT_WITH_MULTIPLE_MERCHANTS` to `ThreeDSecureMerchantInitiatedRequestType`
* Deprecate
    * `AUTHENTICATION_BYPASSED` value for `ThreeDSecureAuthenticationStatus` enum
* Add new field
    `merchantOnRecordname` to `ThreeDSecureLookupTransactionInformationInput`

# 06-13-2024
* Add new field
    * `fastlane` to `ClientConfiguration`
    * `acceptPartialAuthorization` to `InStoreAuthorizationInput`
    * `paymentInitiator` to `InStoreAuthorizationInput`
    * `acceptPartialAuthorization` to `InStoreTransactionInput`
    * `products` to `Merchant`
    * `processingMode` to `PaymentSearchInput`
    * `merchantInitiatedRequest` to `PerformThreeDSecureLookupInput`
    * `processingMode` to `RefundSearchInput`
    * `inStoreLocations` to `Search`
    * `processingMode` to `TransactionSearchInput`
* Add new input
    * `DisableProductForMerchantInput`
    * `EnableProductForMerchantInput`
    * `InStoreLocationAddressSearchInput`
    * `InStoreLocationConditionInput`
    * `InStoreLocationSearchInput`
    * `ProductInput`
    * `SearchProcessingModeInput`
    * `SearchTextValueInput`
    * `ThreeDSecureMerchantInitiatedRequestInput`
    * `ThreeDSecurePriorAuthenticationInput`
* Add new type
    * `DisableProductForMerchantPayload`
    * `EnableProductForMerchantPayload`
    * `FastlaneConfiguration`
    * `InStoreLocationSearchConnection`
    * `Product`
* Add new enum
    * `InStorePaymentInitiator`
    * `ProductCode`
    * `ProductEnablementStatus`
    * `ThreeDSecureMerchantInitiatedRequestType`
* Add new mutation
    * `enableProductForMerchant`
    * `disableProductForMerchant`
* Add new enum value
    * `ESTIMATED` to `PaymentInitiator`
* Deprecate
    * `AUTHENTICATE_SIGNATURE_VERIFICATION_FAILED` enum value for `ThreeDSecureAuthenticationShippingType` enum 

# 04-23-2024
* Update doc string
    * `paymentId` in `CreatePayPalOneTimePaymentPayload`
* Add new input
    * `CreateTransactionPackageTrackingInput`
    * `SearchDisputeMerchantAccountIdInput`
    * `TransactionPackageTrackingLineItemInput`
    * `VenmoPaysheetLineItemInput`
* Add new type
    * `CreateTransactionPackageTrackingPayload`
    * `TransactionPackageTracker`
    * `VenmoPaysheetLineItem`
* Change expected input
    * `merchantAccountId` in `DisputeTransactionSearchInput`
* Add new mutation
    * `createTransactionPackageTracking`
* Add new field
    * `partiallyAuthorized` in `Transaction`, `TransactionSearchInput`
    * `packageTrackers` in `TransactionShipping`
    * `venmoPaysheetLineItems` in `VenmoPaysheetTransactionDetails`, `VenmoPaysheetTransactionDetailsInput`
* Deprecate field
    * `lineItems` in `VenmoPaysheetTransactionDetails`

# 03-26-2024
* Add new enum
    * `InStoreBackgroundStyle`
    * `UpcType`
* Add new input
    * `InStoreChoiceInput`
    * `LineItemUpcInput`
    * `RequestMultiChoiceSingleSelectPromptFromInStoreReaderInput`
    * `SearchPaymentMerchantAccountIdInput`
* Add new type
    * `LineItemsUpc`
    * `RequesyMultiChoiceSingleSelectPromptInStoreContext
* Add new mutation
    * `requestMultiChoiceSingleSelectPromptFromInStoreReader`
* Update type
    * Change `merchantAccountId` in `PaymentSearchInput`, `RefundSearchInput`, `TransactionSearchInput` to `SearchPaymentMerchantAccountIdInput`
* Add new field
    * `imageUrl`, `upc` to `PayPalLineItem` and `PayPalLineItemInput`
    * `upc` to `TransactionLineItem` and `TransactionLineItemInput`

# 02-27-2024

* Add new enum value
    * `CREDIT_ISSUED_ARN` to `DisputeEvidenceCategory` and `DisputeTextEvidenceCategory`
* Deprecate
    * `tokenizeUsBankLogin` mutation
    * `TokenizeUsBankLoginInput`
    * `plaidPublicKey` field under `UsBankAccountBusinessOwnerInput`
    * `UsBankLoginInput`

# 02-06-2024

* Add new field
    * `domains` to `ClientTokenInput`
    * `isFinalAmount` to CreateVenmoPaymentContextInput
    * `isFinalAmount` to VenmoPaymentContext

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
