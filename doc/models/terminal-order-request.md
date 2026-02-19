
# Terminal Order Request

## Structure

`TerminalOrderRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingEntityId` | `?string` | Optional | The identification of the billing entity to use for the order.<br><br>> When ordering products in Brazil, you do not need to include the `billingEntityId` in the request. | getBillingEntityId(): ?string | setBillingEntityId(?string billingEntityId): void |
| `customerOrderReference` | `?string` | Optional | The merchant-defined purchase order reference. | getCustomerOrderReference(): ?string | setCustomerOrderReference(?string customerOrderReference): void |
| `items` | [`?(OrderItem[])`](../../doc/models/order-item.md) | Optional | The products included in the order. | getItems(): ?array | setItems(?array items): void |
| `orderType` | `?string` | Optional | Type of order | getOrderType(): ?string | setOrderType(?string orderType): void |
| `shippingLocationId` | `?string` | Optional | The identification of the shipping location to use for the order. | getShippingLocationId(): ?string | setShippingLocationId(?string shippingLocationId): void |
| `taxId` | `?string` | Optional | The tax number of the billing entity. | getTaxId(): ?string | setTaxId(?string taxId): void |

## Example (as JSON)

```json
{
  "billingEntityId": "billingEntityId6",
  "customerOrderReference": "customerOrderReference8",
  "items": [
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    },
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    },
    {
      "id": "id8",
      "installments": 204,
      "name": "name8",
      "quantity": 22
    }
  ],
  "orderType": "orderType4",
  "shippingLocationId": "shippingLocationId4"
}
```

