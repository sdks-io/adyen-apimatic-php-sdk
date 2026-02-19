
# Billing Entities Response

## Structure

`BillingEntitiesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(BillingEntity[])`](../../doc/models/billing-entity.md) | Optional | List of legal entities that can be used for the billing of orders. | getData(): ?array | setData(?array data): void |

## Example (as JSON)

```json
{
  "data": [
    {
      "address": {
        "city": "city6",
        "companyName": "companyName8",
        "country": "country0",
        "postalCode": "postalCode8",
        "stateOrProvince": "stateOrProvince4"
      },
      "email": "email6",
      "id": "id0",
      "name": "name0",
      "taxId": "taxId6"
    },
    {
      "address": {
        "city": "city6",
        "companyName": "companyName8",
        "country": "country0",
        "postalCode": "postalCode8",
        "stateOrProvince": "stateOrProvince4"
      },
      "email": "email6",
      "id": "id0",
      "name": "name0",
      "taxId": "taxId6"
    },
    {
      "address": {
        "city": "city6",
        "companyName": "companyName8",
        "country": "country0",
        "postalCode": "postalCode8",
        "stateOrProvince": "stateOrProvince4"
      },
      "email": "email6",
      "id": "id0",
      "name": "name0",
      "taxId": "taxId6"
    }
  ]
}
```

