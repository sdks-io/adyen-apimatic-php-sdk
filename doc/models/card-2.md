
# Card 2

The payment method used by the shopper.

## Structure

`Card2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingSequenceNumber` | `?string` | Optional | The sequence number for the debit. For example, send **2** if this is the second debit for the subscription. The sequence number is included in the notification sent to the shopper. | getBillingSequenceNumber(): ?string | setBillingSequenceNumber(?string billingSequenceNumber): void |
| `brand` | `?string` | Optional | Secondary brand of the card. For example: **plastix**, **hmclub**. | getBrand(): ?string | setBrand(?string brand): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `cupsecureplusSmscode` | `?string` | Optional | - | getCupsecureplusSmscode(): ?string | setCupsecureplusSmscode(?string cupsecureplusSmscode): void |
| `cvc` | `?string` | Optional | The card verification code. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getCvc(): ?string | setCvc(?string cvc): void |
| `encryptedCard` | `?string` | Optional | Only include this for JSON Web Encryption (JWE) implementations. The JWE-encrypted card details.<br><br>**Constraints**: *Maximum Length*: `40000` | getEncryptedCard(): ?string | setEncryptedCard(?string encryptedCard): void |
| `encryptedCardNumber` | `?string` | Optional | The encrypted card number.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedCardNumber(): ?string | setEncryptedCardNumber(?string encryptedCardNumber): void |
| `encryptedExpiryMonth` | `?string` | Optional | The encrypted card expiry month.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedExpiryMonth(): ?string | setEncryptedExpiryMonth(?string encryptedExpiryMonth): void |
| `encryptedExpiryYear` | `?string` | Optional | The encrypted card expiry year.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedExpiryYear(): ?string | setEncryptedExpiryYear(?string encryptedExpiryYear): void |
| `encryptedPassword` | `?string` | Optional | This field contains an encrypted, one-time password or an authentication code provided by the cardholder.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedPassword(): ?string | setEncryptedPassword(?string encryptedPassword): void |
| `encryptedSecurityCode` | `?string` | Optional | The encrypted card verification code.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedSecurityCode(): ?string | setEncryptedSecurityCode(?string encryptedSecurityCode): void |
| `expiryMonth` | `?string` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryMonth(): ?string | setExpiryMonth(?string expiryMonth): void |
| `expiryYear` | `?string` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryYear(): ?string | setExpiryYear(?string expiryYear): void |
| `fastlaneData` | `?string` | Optional | The encoded fastlane data blob | getFastlaneData(): ?string | setFastlaneData(?string fastlaneData): void |
| `fundingSource` | [`?string(FundingSource)`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `holderName` | `?string` | Optional | The name of the card holder.<br><br>**Constraints**: *Maximum Length*: `15000` | getHolderName(): ?string | setHolderName(?string holderName): void |
| `networkPaymentReference` | `?string` | Optional | The transaction identifier from card schemes. This is the [`networkTxReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-additionalData-ResponseAdditionalDataCommon-networkTxReference) from the response to the first payment. | getNetworkPaymentReference(): ?string | setNetworkPaymentReference(?string networkPaymentReference): void |
| `number` | `?string` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getNumber(): ?string | setNumber(?string number): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperNotificationReference` | `?string` | Optional | The `shopperNotificationReference` returned in the response when you requested to notify the shopper. Used only for recurring payments in India. | getShopperNotificationReference(): ?string | setShopperNotificationReference(?string shopperNotificationReference): void |
| `srcCorrelationId` | `?string` | Optional | An identifier used for the Click to Pay transaction. | getSrcCorrelationId(): ?string | setSrcCorrelationId(?string srcCorrelationId): void |
| `srcDigitalCardId` | `?string` | Optional | The SRC reference for the Click to Pay token. | getSrcDigitalCardId(): ?string | setSrcDigitalCardId(?string srcDigitalCardId): void |
| `srcScheme` | `?string` | Optional | The scheme that is being used for Click to Pay. | getSrcScheme(): ?string | setSrcScheme(?string srcScheme): void |
| `srcTokenReference` | `?string` | Optional | The reference for the Click to Pay token. | getSrcTokenReference(): ?string | setSrcTokenReference(?string srcTokenReference): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `threeDs2SdkVersion` | `?string` | Optional | Required for mobile integrations. Version of the 3D Secure 2 mobile SDK.<br><br>**Constraints**: *Maximum Length*: `12` | getThreeDs2SdkVersion(): ?string | setThreeDs2SdkVersion(?string threeDs2SdkVersion): void |
| `type` | [`?string(Type12)`](../../doc/models/type-12.md) | Optional | Default payment method details. Common for scheme payment methods, and for simple payment method details.<br><br>**Default**: `Type12::SCHEME` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "scheme",
  "billingSequenceNumber": "billingSequenceNumber8",
  "brand": "brand2",
  "checkoutAttemptId": "checkoutAttemptId4",
  "cupsecureplus.smscode": "cupsecureplus.smscode6",
  "cvc": "cvc2"
}
```

