
# Stored Payment Method 1

## Structure

`StoredPaymentMethod1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `string` | Required | The issuer id of the shopper's selected bank. | getIssuer(): string | setIssuer(string issuer): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`string(Type26)`](../../doc/models/type-26.md) | Required | **genericissuer** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId4",
  "issuer": "issuer8",
  "recurringDetailReference": "recurringDetailReference8",
  "sdkData": "sdkData2",
  "storedPaymentMethodId": "storedPaymentMethodId2",
  "type": "onlineBanking_CZ"
}
```

