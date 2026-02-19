
# Response Additional Data Card

## Structure

`ResponseAdditionalDataCard`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cardBin` | `?string` | Optional | The first six digits of the card number.<br><br>This is the [Bank Identification Number (BIN)](https://docs.adyen.com/get-started-with-adyen/payment-glossary#bank-identification-number-bin) for card numbers with a six-digit BIN.<br><br>Example: 521234 | getCardBin(): ?string | setCardBin(?string cardBin): void |
| `cardHolderName` | `?string` | Optional | The cardholder name passed in the payment request. | getCardHolderName(): ?string | setCardHolderName(?string cardHolderName): void |
| `cardIssuingBank` | `?string` | Optional | The bank or the financial institution granting lines of credit through card association branded payment cards. This information can be included when available. | getCardIssuingBank(): ?string | setCardIssuingBank(?string cardIssuingBank): void |
| `cardIssuingCountry` | `?string` | Optional | The country where the card was issued.<br><br>Example: US | getCardIssuingCountry(): ?string | setCardIssuingCountry(?string cardIssuingCountry): void |
| `cardIssuingCurrency` | `?string` | Optional | The currency in which the card is issued, if this information is available. Provided as the currency code or currency number from the ISO-4217 standard.<br><br>Example: USD | getCardIssuingCurrency(): ?string | setCardIssuingCurrency(?string cardIssuingCurrency): void |
| `cardPaymentMethod` | `?string` | Optional | The card payment method used for the transaction.<br><br>Example: amex | getCardPaymentMethod(): ?string | setCardPaymentMethod(?string cardPaymentMethod): void |
| `cardProductId` | [`?string(CardProductId)`](../../doc/models/card-product-id.md) | Optional | The Card Product ID represents the type of card following card scheme product definitions and can be returned for Adyen Acquiring service level payments.<br><br>Possible values Visa:<br><br>* **A** - Visa Traditional<br>* **B** - Visa Traditional Rewards<br>* **C** - Visa Signature<br>* **D** - Visa Signature Preferred<br>* **F** - Visa Classic<br><br>Possible values Mastercard:<br><br>* **MCC** - Mastercard Card<br>* **MCE** - Mastercard Electronic Card<br>* **MCF** - Mastercard Corporate Fleet Card<br>* **MCG** - Gold Mastercard Card<br>* **MCH** - Mastercard Premium Charge<br>* **MCI** - Mastercard Select Debit | getCardProductId(): ?string | setCardProductId(?string cardProductId): void |
| `cardSummary` | `?string` | Optional | The last four digits of a card number.<br><br>> Returned only in case of a card payment. | getCardSummary(): ?string | setCardSummary(?string cardSummary): void |
| `issuerBin` | `?string` | Optional | The first eight digits of the card number. Only returned if the card number is 16 digits or more.<br><br>This is the [Bank Identification Number (BIN)](https://docs.adyen.com/get-started-with-adyen/payment-glossary#bank-identification-number-bin) for card numbers with an eight-digit BIN.<br><br>Example: 52123423 | getIssuerBin(): ?string | setIssuerBin(?string issuerBin): void |

## Example (as JSON)

```json
{
  "cardBin": "cardBin4",
  "cardHolderName": "cardHolderName2",
  "cardIssuingBank": "cardIssuingBank4",
  "cardIssuingCountry": "cardIssuingCountry4",
  "cardIssuingCurrency": "cardIssuingCurrency2"
}
```

