
# Billing Entity 1

The details of the entity that the order is billed to.

## Structure

`BillingEntity1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `address` | [`?Address11`](../../doc/models/address-11.md) | Optional | The address details of the billing entity. | getAddress(): ?Address11 | setAddress(?Address11 address): void |
| `email` | `?string` | Optional | The email address of the billing entity. | getEmail(): ?string | setEmail(?string email): void |
| `id` | `?string` | Optional | The unique identifier of the billing entity, for use as `billingEntityId` when creating an order. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The unique name of the billing entity. | getName(): ?string | setName(?string name): void |
| `taxId` | `?string` | Optional | The tax number of the billing entity. | getTaxId(): ?string | setTaxId(?string taxId): void |

## Example (as JSON)

```json
{
  "address": {
    "city": "city6",
    "companyName": "companyName8",
    "country": "country0",
    "postalCode": "postalCode8",
    "stateOrProvince": "stateOrProvince4"
  },
  "email": "email0",
  "id": "id6",
  "name": "name6",
  "taxId": "taxId2"
}
```

