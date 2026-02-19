
# Affirm Info

## Structure

`AffirmInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricePlan` | [`?string(PricePlan)`](../../doc/models/price-plan.md) | Optional | Merchant price plan | getPricePlan(): ?string | setPricePlan(?string pricePlan): void |
| `supportEmail` | `string` | Required | Merchant support email | getSupportEmail(): string | setSupportEmail(string supportEmail): void |

## Example (as JSON)

```json
{
  "pricePlan": "GOLD",
  "supportEmail": "supportEmail0"
}
```

