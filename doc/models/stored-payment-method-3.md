
# Stored Payment Method 3

*This model accepts additional fields of type array.*

## Structure

`StoredPaymentMethod3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `pixRecurring` | [`?PixRecurring`](../../doc/models/pix-recurring.md) | Optional | - | getPixRecurring(): ?PixRecurring | setPixRecurring(?PixRecurring pixRecurring): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type39)`](../../doc/models/type-39.md) | Optional | The payment method type. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId8",
  "pixRecurring": {
    "billingDate": "billingDate0",
    "businessDayOnly": false,
    "endsAt": "endsAt8",
    "frequency": "yearly",
    "minAmount": {
      "currency": "currency6",
      "value": 156
    }
  },
  "recurringDetailReference": "recurringDetailReference2",
  "sdkData": "sdkData8",
  "storedPaymentMethodId": "storedPaymentMethodId6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

