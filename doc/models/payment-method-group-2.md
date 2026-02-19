
# Payment Method Group 2

The group where this payment method belongs to.

## Structure

`PaymentMethodGroup2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the group. | getName(): ?string | setName(?string name): void |
| `paymentMethodData` | `?string` | Optional | Echo data to be used if the payment method is displayed as part of this group. | getPaymentMethodData(): ?string | setPaymentMethodData(?string paymentMethodData): void |
| `type` | `?string` | Optional | The unique code of the group. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "name": "name2",
  "paymentMethodData": "paymentMethodData6",
  "type": "type8"
}
```

