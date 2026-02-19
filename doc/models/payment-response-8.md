
# Payment Response 8

## Structure

`PaymentResponse8`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brand` | `?string` | Optional | The card brand that the shopper used to pay. Only returned if `paymentMethod.type` is **scheme**. | getBrand(): ?string | setBrand(?string brand): void |
| `type` | `?string` | Optional | The `paymentMethod.type` value used in the request. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "brand": "brand6",
  "type": "type8"
}
```

