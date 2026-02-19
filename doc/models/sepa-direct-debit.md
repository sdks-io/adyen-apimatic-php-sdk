
# Sepa Direct Debit

*This model accepts additional fields of type array.*

## Structure

`SepaDirectDebit`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `dueDate` | `?string` | Optional | The date that the the shopper's bank account is charged. | getDueDate(): ?string | setDueDate(?string dueDate): void |
| `iban` | `string` | Required | The International Bank Account Number (IBAN). | getIban(): string | setIban(string iban): void |
| `ownerName` | `string` | Required | The name of the bank account holder. | getOwnerName(): string | setOwnerName(string ownerName): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `transferInstrumentId` | `?string` | Optional | The unique identifier of your user's verified transfer instrument, which you can use to top up their balance accounts. | getTransferInstrumentId(): ?string | setTransferInstrumentId(?string transferInstrumentId): void |
| `type` | [`?string(Type45)`](../../doc/models/type-45.md) | Optional | **sepadirectdebit**<br><br>**Default**: `Type45::SEPADIRECTDEBIT` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "iban": "iban4",
  "ownerName": "ownerName4",
  "type": "sepadirectdebit",
  "checkoutAttemptId": "checkoutAttemptId6",
  "dueDate": "dueDate6",
  "recurringDetailReference": "recurringDetailReference0",
  "sdkData": "sdkData0",
  "storedPaymentMethodId": "storedPaymentMethodId4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

