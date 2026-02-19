
# Pay Me Info 1

Details to provide if `type` is **payme**.

## Structure

`PayMeInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `displayName` | `string` | Required | Merchant display name | getDisplayName(): string | setDisplayName(string displayName): void |
| `logo` | `string` | Required | Merchant logo. Format: Base64-encoded string. | getLogo(): string | setLogo(string logo): void |
| `supportEmail` | `string` | Required | The email address of merchant support. | getSupportEmail(): string | setSupportEmail(string supportEmail): void |

## Example (as JSON)

```json
{
  "displayName": "displayName8",
  "logo": "logo0",
  "supportEmail": "supportEmail0"
}
```

