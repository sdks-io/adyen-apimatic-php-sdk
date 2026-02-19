
# Pay Pal

## Structure

`PayPal`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `orderId` | `?string` | Optional | The unique ID associated with the order. | getOrderId(): ?string | setOrderId(?string orderId): void |
| `payeePreferred` | `?string` | Optional | IMMEDIATE_PAYMENT_REQUIRED or UNRESTRICTED | getPayeePreferred(): ?string | setPayeePreferred(?string payeePreferred): void |
| `payerId` | `?string` | Optional | The unique ID associated with the payer. | getPayerId(): ?string | setPayerId(?string payerId): void |
| `payerSelected` | `?string` | Optional | PAYPAL or PAYPAL_CREDIT | getPayerSelected(): ?string | setPayerSelected(?string payerSelected): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `subtype` | [`?string(Subtype)`](../../doc/models/subtype.md) | Optional | The type of flow to initiate. | getSubtype(): ?string | setSubtype(?string subtype): void |
| `type` | `string` | Required, Constant | **paypal**<br><br>**Value**: `'paypal'` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "type": "paypal",
  "checkoutAttemptId": "checkoutAttemptId2",
  "orderID": "orderID0",
  "payeePreferred": "payeePreferred6",
  "payerID": "payerID2",
  "payerSelected": "payerSelected2"
}
```

