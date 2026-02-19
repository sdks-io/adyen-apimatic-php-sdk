
# Checkout Order Response 1

Contains updated information regarding the order in case order information was provided in the request.

## Structure

`CheckoutOrderResponse1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`?Amount11`](../../doc/models/amount-11.md) | Optional | The initial amount of the order. | getAmount(): ?Amount11 | setAmount(?Amount11 amount): void |
| `expiresAt` | `?string` | Optional | The expiry date for the order. | getExpiresAt(): ?string | setExpiresAt(?string expiresAt): void |
| `orderData` | `?string` | Optional | The encrypted order data. | getOrderData(): ?string | setOrderData(?string orderData): void |
| `pspReference` | `string` | Required | The `pspReference` that belongs to the order. | getPspReference(): string | setPspReference(string pspReference): void |
| `reference` | `?string` | Optional | The merchant reference for the order. | getReference(): ?string | setReference(?string reference): void |
| `remainingAmount` | [`?Amount12`](../../doc/models/amount-12.md) | Optional | The updated remaining amount. | getRemainingAmount(): ?Amount12 | setRemainingAmount(?Amount12 remainingAmount): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt0",
  "orderData": "orderData6",
  "pspReference": "pspReference6",
  "reference": "reference0",
  "remainingAmount": {
    "currency": "currency6",
    "value": 156
  }
}
```

