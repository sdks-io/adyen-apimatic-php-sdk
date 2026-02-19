
# Shopper Tax Info

## Structure

`ShopperTaxInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `taxId` | `string` | Required | The tax-id of the shopper doing the transaction.<br><br>**Constraints**: *Maximum Length*: `10` | getTaxId(): string | setTaxId(string taxId): void |
| `taxIdCountryCode` | `string` | Required | The country to which the tax-id belongs to.<br><br>**Constraints**: *Maximum Length*: `2` | getTaxIdCountryCode(): string | setTaxIdCountryCode(string taxIdCountryCode): void |

## Example (as JSON)

```json
{
  "taxId": "taxId6",
  "taxIdCountryCode": "taxIdCountryCode2"
}
```

