
# Checkout Forward Request Card 2

The card details.

## Structure

`CheckoutForwardRequestCard2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cvc` | `?string` | Optional | The [card verification code](https://docs.adyen.com/payments-fundamentals/payment-glossary#card-security-code-cvc-cvv-cid) (1-20 characters). Depending on the card brand, it is also known as:<br><br>* CVV2/CVC2 – length: 3 digits<br>* CID – length: 4 digits | getCvc(): ?string | setCvc(?string cvc): void |
| `encryptedCardNumber` | `?string` | Optional | The encrypted card number. | getEncryptedCardNumber(): ?string | setEncryptedCardNumber(?string encryptedCardNumber): void |
| `encryptedExpiryMonth` | `?string` | Optional | The encrypted expiryMonth | getEncryptedExpiryMonth(): ?string | setEncryptedExpiryMonth(?string encryptedExpiryMonth): void |
| `encryptedExpiryYear` | `?string` | Optional | The encrypted card expiry year. | getEncryptedExpiryYear(): ?string | setEncryptedExpiryYear(?string encryptedExpiryYear): void |
| `encryptedSecurityCode` | `?string` | Optional | The encrypted security code. | getEncryptedSecurityCode(): ?string | setEncryptedSecurityCode(?string encryptedSecurityCode): void |
| `expiryMonth` | `?string` | Optional | The card expiry month.<br>Format: 2 digits, zero-padded for single digits. For example:<br><br>* 03 = March<br>* 11 = November | getExpiryMonth(): ?string | setExpiryMonth(?string expiryMonth): void |
| `expiryYear` | `?string` | Optional | The card expiry year. | getExpiryYear(): ?string | setExpiryYear(?string expiryYear): void |
| `holderName` | `?string` | Optional | The name of the cardholder. | getHolderName(): ?string | setHolderName(?string holderName): void |
| `number` | `?string` | Optional | The card number. Only collect raw card data if you are fully [PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide).<br>Format: Do not use separators. | getNumber(): ?string | setNumber(?string number): void |
| `type` | [`?string(Type16)`](../../doc/models/type-16.md) | Optional | Default payment method details. Common for scheme payment methods, and for simple payment method details.<br><br>**Default**: `Type16::SCHEME` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "scheme",
  "cvc": "cvc6",
  "encryptedCardNumber": "encryptedCardNumber0",
  "encryptedExpiryMonth": "encryptedExpiryMonth8",
  "encryptedExpiryYear": "encryptedExpiryYear2",
  "encryptedSecurityCode": "encryptedSecurityCode8"
}
```

