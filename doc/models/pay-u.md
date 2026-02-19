
# Pay U

## Structure

`PayU`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperNotificationReference` | `?string` | Optional | The `shopperNotificationReference` returned in the response when you requested to notify the shopper. Used for recurring payment only. | getShopperNotificationReference(): ?string | setShopperNotificationReference(?string shopperNotificationReference): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | `string` | Required, Constant | **payu_IN_upi**<br><br>**Value**: `'payu_IN_upi'` | getType(): string | setType(string type): void |
| `virtualPaymentAddress` | `?string` | Optional | The virtual payment address for UPI. | getVirtualPaymentAddress(): ?string | setVirtualPaymentAddress(?string virtualPaymentAddress): void |

## Example (as JSON)

```json
{
  "type": "payu_IN_upi",
  "checkoutAttemptId": "checkoutAttemptId8",
  "recurringDetailReference": "recurringDetailReference2",
  "sdkData": "sdkData8",
  "shopperNotificationReference": "shopperNotificationReference2",
  "storedPaymentMethodId": "storedPaymentMethodId6"
}
```

