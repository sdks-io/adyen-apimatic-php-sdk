
# Shipping Location 1

The details of the location where the order is shipped to.

## Structure

`ShippingLocation1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `address` | [`?Address21`](../../doc/models/address-21.md) | Optional | The address details of the shipping location. | getAddress(): ?Address21 | setAddress(?Address21 address): void |
| `contact` | [`?Contact1`](../../doc/models/contact-1.md) | Optional | The contact details for the shipping location. | getContact(): ?Contact1 | setContact(?Contact1 contact): void |
| `id` | `?string` | Optional | The unique identifier of the shipping location, for use as `shippingLocationId` when creating an order. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The unique name of the shipping location. | getName(): ?string | setName(?string name): void |

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
  "contact": {
    "email": "email4",
    "firstName": "firstName2",
    "infix": "infix6",
    "lastName": "lastName6",
    "phoneNumber": "phoneNumber2"
  },
  "id": "id6",
  "name": "name6"
}
```

