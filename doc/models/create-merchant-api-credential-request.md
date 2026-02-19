
# Create Merchant Api Credential Request

## Structure

`CreateMerchantApiCredentialRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allowedOrigins` | `?(string[])` | Optional | The list of [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) for the new API credential. | getAllowedOrigins(): ?array | setAllowedOrigins(?array allowedOrigins): void |
| `description` | `?string` | Optional | Description of the API credential. | getDescription(): ?string | setDescription(?string description): void |
| `roles` | `?(string[])` | Optional | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. Only roles assigned to 'ws@Company.<CompanyName>' can be assigned to other API credentials. | getRoles(): ?array | setRoles(?array roles): void |

## Example (as JSON)

```json
{
  "allowedOrigins": [
    "allowedOrigins4",
    "allowedOrigins3"
  ],
  "description": "description4",
  "roles": [
    "roles0",
    "roles1"
  ]
}
```

