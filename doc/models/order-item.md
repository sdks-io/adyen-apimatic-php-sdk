
# Order Item

## Structure

`OrderItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | The unique identifier of the product. | getId(): ?string | setId(?string id): void |
| `installments` | `?int` | Optional | The number of installments for the specified product `id`. | getInstallments(): ?int | setInstallments(?int installments): void |
| `name` | `?string` | Optional | The name of the product. | getName(): ?string | setName(?string name): void |
| `quantity` | `?int` | Optional | The number of items with the specified product `id` included in the order. | getQuantity(): ?int | setQuantity(?int quantity): void |

## Example (as JSON)

```json
{
  "id": "id2",
  "installments": 214,
  "name": "name2",
  "quantity": 32
}
```

