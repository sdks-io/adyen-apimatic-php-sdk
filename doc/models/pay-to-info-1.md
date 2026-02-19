
# Pay to Info 1

Details to provide if `type` is **payto**.

## Structure

`PayToInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantName` | `string` | Required | Merchant name displayed to the shopper in the Agreements | getMerchantName(): string | setMerchantName(string merchantName): void |
| `payToPurpose` | `string` | Required | Represents the purpose of the Agreements created, it relates to the business type<br>**Allowed values**: mortgage, utility, loan, gambling, retail, salary, personal, government, pension, tax, other | getPayToPurpose(): string | setPayToPurpose(string payToPurpose): void |

## Example (as JSON)

```json
{
  "merchantName": "merchantName8",
  "payToPurpose": "payToPurpose6"
}
```

