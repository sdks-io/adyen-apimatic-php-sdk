
# Details of Tokens That Are Not Stored With Adyen

## Structure

`DetailsOfTokensThatAreNotStoredWithAdyen`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `expiryMonth` | `?string` | Optional | The card expiry month. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryMonth(): ?string | setExpiryMonth(?string expiryMonth): void |
| `expiryYear` | `?string` | Optional | The card expiry year. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getExpiryYear(): ?string | setExpiryYear(?string expiryYear): void |
| `holderName` | `?string` | Optional | The name of the card holder.<br><br>**Constraints**: *Maximum Length*: `15000` | getHolderName(): ?string | setHolderName(?string holderName): void |
| `number` | `?string` | Optional | The card number. Only collect raw card data if you are [fully PCI compliant](https://docs.adyen.com/development-resources/pci-dss-compliance-guide). | getNumber(): ?string | setNumber(?string number): void |
| `storedPaymentMethodId` | `string` | Required | Identifier used to fetch the token from the external service<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): string | setStoredPaymentMethodId(string storedPaymentMethodId): void |
| `subtype` | `string` | Required, Constant | The external service from which to fetch the token. Supported only for specific companies. Contact Adyen if you want to use this feature.<br><br>**Value**: `'hilton'` | getSubtype(): string | setSubtype(string subtype): void |
| `type` | `string` | Required, Constant | The type of token. Allowed value: **externalToken**.<br><br>**Value**: `'externalToken'` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "storedPaymentMethodId": "storedPaymentMethodId8",
  "subtype": "hilton",
  "type": "externalToken",
  "checkoutAttemptId": "checkoutAttemptId0",
  "expiryMonth": "expiryMonth8",
  "expiryYear": "expiryYear8",
  "holderName": "holderName0",
  "number": "number2"
}
```

