
# Afterpay

## Structure

`Afterpay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingAddress` | `?string` | Optional | The address where to send the invoice. | getBillingAddress(): ?string | setBillingAddress(?string billingAddress): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `deliveryAddress` | `?string` | Optional | The address where the goods should be delivered. | getDeliveryAddress(): ?string | setDeliveryAddress(?string deliveryAddress): void |
| `personalDetails` | `?string` | Optional | Shopper name, date of birth, phone number, and email address. | getPersonalDetails(): ?string | setPersonalDetails(?string personalDetails): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`string(Type2)`](../../doc/models/type-2.md) | Required | **afterpay_default**<br><br>**Default**: `Type2::AFTERPAY_DEFAULT` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "type": "afterpay_default",
  "billingAddress": "billingAddress8",
  "checkoutAttemptId": "checkoutAttemptId0",
  "deliveryAddress": "deliveryAddress0",
  "personalDetails": "personalDetails2",
  "recurringDetailReference": "recurringDetailReference4"
}
```

