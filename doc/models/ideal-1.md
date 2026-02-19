
# Ideal 1

## Structure

`Ideal1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `?string` | Optional | The iDEAL issuer value of the shopper's selected bank. Set this to an **id** of an iDEAL issuer to preselect it. | getIssuer(): ?string | setIssuer(?string issuer): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type21)`](../../doc/models/type-21.md) | Optional | **ideal**<br><br>**Default**: `Type21::IDEAL` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "ideal",
  "checkoutAttemptId": "checkoutAttemptId6",
  "issuer": "issuer0",
  "recurringDetailReference": "recurringDetailReference0",
  "sdkData": "sdkData0",
  "storedPaymentMethodId": "storedPaymentMethodId4"
}
```

