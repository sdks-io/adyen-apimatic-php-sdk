
# Payment Method to Store 1

Contains the information required to store a payment method.

## Structure

`PaymentMethodToStore1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brand` | `?string` | Optional | Secondary brand of the card. For example: **plastix**, **hmclub**. | getBrand(): ?string | setBrand(?string brand): void |
| `cvc` | `?string` | Optional | The card verification code. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getCvc(): ?string | setCvc(?string cvc): void |
| `encryptedCard` | `?string` | Optional | The encrypted card.<br><br>**Constraints**: *Maximum Length*: `40000` | getEncryptedCard(): ?string | setEncryptedCard(?string encryptedCard): void |
| `encryptedCardNumber` | `?string` | Optional | The encrypted card number.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedCardNumber(): ?string | setEncryptedCardNumber(?string encryptedCardNumber): void |
| `encryptedExpiryMonth` | `?string` | Optional | The encrypted card expiry month.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedExpiryMonth(): ?string | setEncryptedExpiryMonth(?string encryptedExpiryMonth): void |
| `encryptedExpiryYear` | `?string` | Optional | The encrypted card expiry year.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedExpiryYear(): ?string | setEncryptedExpiryYear(?string encryptedExpiryYear): void |
| `encryptedSecurityCode` | `?string` | Optional | The encrypted card verification code.<br><br>**Constraints**: *Maximum Length*: `15000` | getEncryptedSecurityCode(): ?string | setEncryptedSecurityCode(?string encryptedSecurityCode): void |
| `expiryMonth` | `?string` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryMonth(): ?string | setExpiryMonth(?string expiryMonth): void |
| `expiryYear` | `?string` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryYear(): ?string | setExpiryYear(?string expiryYear): void |
| `holderName` | `?string` | Optional | The name of the card holder. | getHolderName(): ?string | setHolderName(?string holderName): void |
| `number` | `?string` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getNumber(): ?string | setNumber(?string number): void |
| `type` | `?string` | Optional | Set to **scheme**. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "brand": "brand2",
  "cvc": "cvc2",
  "encryptedCard": "encryptedCard0",
  "encryptedCardNumber": "encryptedCardNumber6",
  "encryptedExpiryMonth": "encryptedExpiryMonth4"
}
```

