
# Pay To

## Structure

`PayTo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperAccountIdentifier` | `?string` | Optional | The shopper's banking details or payId reference, used to complete payment. | getShopperAccountIdentifier(): ?string | setShopperAccountIdentifier(?string shopperAccountIdentifier): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type36)`](../../doc/models/type-36.md) | Optional | **payto**<br><br>**Default**: `Type36::PAYTO` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "payto",
  "checkoutAttemptId": "checkoutAttemptId2",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData4",
  "shopperAccountIdentifier": "shopperAccountIdentifier6",
  "storedPaymentMethodId": "storedPaymentMethodId0"
}
```

