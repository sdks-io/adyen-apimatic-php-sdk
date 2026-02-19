
# Payment Response 1

Details about the payment method used in the transaction.
Only returned if `resultCode` is **Authorised**.

## Structure

`PaymentResponse1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brand` | `?string` | Optional | The card brand that the shopper used to pay. Only returned if `paymentMethod.type` is **scheme**. | getBrand(): ?string | setBrand(?string brand): void |
| `type` | `?string` | Optional | The `paymentMethod.type` value used in the request. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "brand": "brand2",
  "type": "type2"
}
```

