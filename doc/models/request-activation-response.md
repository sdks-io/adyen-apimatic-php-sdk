
# Request Activation Response

## Structure

`RequestActivationResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `companyId` | `?string` | Optional | The unique identifier of the company account. | getCompanyId(): ?string | setCompanyId(?string companyId): void |
| `merchantId` | `?string` | Optional | The unique identifier of the merchant account you requested to activate. | getMerchantId(): ?string | setMerchantId(?string merchantId): void |

## Example (as JSON)

```json
{
  "companyId": "companyId6",
  "merchantId": "merchantId2"
}
```

