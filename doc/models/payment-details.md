
# Payment Details

## Structure

`PaymentDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type38)`](../../doc/models/type-38.md) | Optional | The payment method type. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId2",
  "sdkData": "sdkData4",
  "type": "molpay_boost"
}
```

