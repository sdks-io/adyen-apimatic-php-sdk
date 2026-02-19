
# Stored Payment Method Resource

## Structure

`StoredPaymentMethodResource`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brand` | `?string` | Optional | The brand of the card. | getBrand(): ?string | setBrand(?string brand): void |
| `cardBin` | `?string` | Optional | The bank identification number (BIN) of the card. | getCardBin(): ?string | setCardBin(?string cardBin): void |
| `expiryMonth` | `?string` | Optional | The month the card expires. | getExpiryMonth(): ?string | setExpiryMonth(?string expiryMonth): void |
| `expiryYear` | `?string` | Optional | The last two digits of the year the card expires. For example, **22** for the year 2022. | getExpiryYear(): ?string | setExpiryYear(?string expiryYear): void |
| `externalResponseCode` | `?string` | Optional | The response code returned by an external system (for example after a provisioning operation). | getExternalResponseCode(): ?string | setExternalResponseCode(?string externalResponseCode): void |
| `externalTokenReference` | `?string` | Optional | The token reference of a linked token in an external system (for example a network token reference). | getExternalTokenReference(): ?string | setExternalTokenReference(?string externalTokenReference): void |
| `holderName` | `?string` | Optional | The unique payment method code. | getHolderName(): ?string | setHolderName(?string holderName): void |
| `iban` | `?string` | Optional | The IBAN of the bank account. | getIban(): ?string | setIban(?string iban): void |
| `id` | `?string` | Optional | A unique identifier of this stored payment method. | getId(): ?string | setId(?string id): void |
| `issuerName` | `?string` | Optional | The name of the issuer of token or card. | getIssuerName(): ?string | setIssuerName(?string issuerName): void |
| `lastFour` | `?string` | Optional | The last four digits of the PAN. | getLastFour(): ?string | setLastFour(?string lastFour): void |
| `mandate` | [`?TokenMandate2`](../../doc/models/token-mandate-2.md) | Optional | Mandate details for the stored payment method. | getMandate(): ?TokenMandate2 | setMandate(?TokenMandate2 mandate): void |
| `name` | `?string` | Optional | The display name of the stored payment method. | getName(): ?string | setName(?string name): void |
| `networkTxReference` | `?string` | Optional | Returned in the response if you are not tokenizing with Adyen and are using the Merchant-initiated transactions (MIT) framework from Mastercard or Visa.<br><br>This contains either the Mastercard Trace ID or the Visa Transaction ID. | getNetworkTxReference(): ?string | setNetworkTxReference(?string networkTxReference): void |
| `ownerName` | `?string` | Optional | The name of the bank account holder. | getOwnerName(): ?string | setOwnerName(?string ownerName): void |
| `shopperEmail` | `?string` | Optional | The shopper’s email address. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `shopperReference` | `?string` | Optional | Your reference to uniquely identify this shopper, for example user ID or account ID. The value is case-sensitive and must be at least three characters.<br><br>> Your reference must not include personally identifiable information (PII) such as name or email address.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `256` | getShopperReference(): ?string | setShopperReference(?string shopperReference): void |
| `supportedRecurringProcessingModels` | `?(string[])` | Optional | Defines a recurring payment type.<br>Allowed values:<br><br>* `Subscription` – A transaction for a fixed or variable amount, which follows a fixed schedule.<br>* `CardOnFile` – With a card-on-file (CoF) transaction, card details are stored to enable one-click or omnichannel journeys, or simply to streamline the checkout process. Any subscription not following a fixed schedule is also considered a card-on-file transaction.<br>* `UnscheduledCardOnFile` – An unscheduled card-on-file (UCoF) transaction is a transaction that occurs on a non-fixed schedule and/or have variable amounts. For example, automatic top-ups when a cardholder's balance drops below a certain amount. | getSupportedRecurringProcessingModels(): ?array | setSupportedRecurringProcessingModels(?array supportedRecurringProcessingModels): void |
| `type` | `?string` | Optional | The type of payment method. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "brand": "brand0",
  "cardBin": "cardBin2",
  "expiryMonth": "expiryMonth0",
  "expiryYear": "expiryYear0",
  "externalResponseCode": "externalResponseCode0"
}
```

