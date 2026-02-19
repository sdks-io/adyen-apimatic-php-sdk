
# Response Additional Data Opi

## Structure

`ResponseAdditionalDataOpi`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `opiTransToken` | `?string` | Optional | Returned in the response if you included `opi.includeTransToken: true` in an ecommerce payment request. This contains an Oracle Payment Interface token that you can store in your Oracle Opera database to identify tokenized ecommerce transactions. For more information and required settings, see [Oracle Opera](https://docs.adyen.com/plugins/oracle-opera#opi-token-ecommerce). | getOpiTransToken(): ?string | setOpiTransToken(?string opiTransToken): void |

## Example (as JSON)

```json
{
  "opi.transToken": "opi.transToken4"
}
```

