
# Delivery Method

## Structure

`DeliveryMethod`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`?Amount23`](../../doc/models/amount-23.md) | Optional | The cost of this delivery method. | getAmount(): ?Amount23 | setAmount(?Amount23 amount): void |
| `description` | `?string` | Optional | The name of the delivery method as shown to the shopper. | getDescription(): ?string | setDescription(?string description): void |
| `reference` | `?string` | Optional | The reference of the delivery method. | getReference(): ?string | setReference(?string reference): void |
| `selected` | `?bool` | Optional | If you display the PayPal lightbox with delivery methods, set to **true** for the delivery method that is selected. Only one delivery method can be selected at a time. | getSelected(): ?bool | setSelected(?bool selected): void |
| `type` | [`?string(Type18)`](../../doc/models/type-18.md) | Optional | The type of the delivery method. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "description": "description6",
  "reference": "reference0",
  "selected": false,
  "type": "Shipping"
}
```

