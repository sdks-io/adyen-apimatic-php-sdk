
# Payment Method Group

## Structure

`PaymentMethodGroup`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the group. | getName(): ?string | setName(?string name): void |
| `paymentMethodData` | `?string` | Optional | Echo data to be used if the payment method is displayed as part of this group. | getPaymentMethodData(): ?string | setPaymentMethodData(?string paymentMethodData): void |
| `type` | `?string` | Optional | The unique code of the group. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "name": "name0",
  "paymentMethodData": "paymentMethodData4",
  "type": "type0"
}
```

