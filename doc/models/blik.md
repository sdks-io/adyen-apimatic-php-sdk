
# Blik

## Structure

`Blik`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blikCode` | `?string` | Optional | BLIK code consisting of 6 digits. | getBlikCode(): ?string | setBlikCode(?string blikCode): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type11)`](../../doc/models/type-11.md) | Optional | **blik** | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "blikCode": "blikCode4",
  "checkoutAttemptId": "checkoutAttemptId2",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData4",
  "storedPaymentMethodId": "storedPaymentMethodId0"
}
```

