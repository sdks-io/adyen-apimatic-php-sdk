
# Stored Payment Method

## Structure

`StoredPaymentMethod`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cashtag` | `?string` | Optional | Cash App issued cashtag for recurring payment | getCashtag(): ?string | setCashtag(?string cashtag): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `customerId` | `?string` | Optional | Cash App issued customerId for recurring payment | getCustomerId(): ?string | setCustomerId(?string customerId): void |
| `grantId` | `?string` | Optional | Cash App issued grantId for one time payment | getGrantId(): ?string | setGrantId(?string grantId): void |
| `onFileGrantId` | `?string` | Optional | Cash App issued onFileGrantId for recurring payment | getOnFileGrantId(): ?string | setOnFileGrantId(?string onFileGrantId): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `requestId` | `?string` | Optional | Cash App request id | getRequestId(): ?string | setRequestId(?string requestId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `subtype` | `?string` | Optional | The payment method subtype. | getSubtype(): ?string | setSubtype(?string subtype): void |
| `type` | [`?string(Type14)`](../../doc/models/type-14.md) | Optional | cashapp<br><br>**Default**: `Type14::CASHAPP` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "cashapp",
  "cashtag": "cashtag0",
  "checkoutAttemptId": "checkoutAttemptId8",
  "customerId": "customerId6",
  "grantId": "grantId0",
  "onFileGrantId": "onFileGrantId0"
}
```

