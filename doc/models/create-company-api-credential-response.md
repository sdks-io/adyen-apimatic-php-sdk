
# Create Company Api Credential Response

## Structure

`CreateCompanyApiCredentialResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?ApiCredentialLinks2`](../../doc/models/api-credential-links-2.md) | Optional | References to resources linked to the API credential. | getLinks(): ?ApiCredentialLinks2 | setLinks(?ApiCredentialLinks2 links): void |
| `active` | `bool` | Required | Indicates if the API credential is enabled. Must be set to **true** to use the credential in your integration. | getActive(): bool | setActive(bool active): void |
| `allowedIpAddresses` | `string[]` | Required | List of IP addresses from which your client can make requests.<br><br>If the list is empty, we allow requests from any IP.<br>If the list is not empty and we get a request from an IP which is not on the list, you get a security error. | getAllowedIpAddresses(): array | setAllowedIpAddresses(array allowedIpAddresses): void |
| `allowedOrigins` | [`?(AllowedOrigin[])`](../../doc/models/allowed-origin.md) | Optional | List containing the [allowed origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins) linked to the API credential. | getAllowedOrigins(): ?array | setAllowedOrigins(?array allowedOrigins): void |
| `apiKey` | `string` | Required | The API key for the API credential that was created. | getApiKey(): string | setApiKey(string apiKey): void |
| `associatedMerchantAccounts` | `string[]` | Required | List of merchant accounts that the API credential has access to. | getAssociatedMerchantAccounts(): array | setAssociatedMerchantAccounts(array associatedMerchantAccounts): void |
| `clientKey` | `string` | Required | Public key used for [client-side authentication](https://docs.adyen.com/development-resources/client-side-authentication). The client key is required for Drop-in and Components integrations. | getClientKey(): string | setClientKey(string clientKey): void |
| `description` | `?string` | Optional | Description of the API credential.<br><br>**Constraints**: *Maximum Length*: `50` | getDescription(): ?string | setDescription(?string description): void |
| `id` | `string` | Required | Unique identifier of the API credential. | getId(): string | setId(string id): void |
| `password` | `string` | Required | The password for the API credential that was created. | getPassword(): string | setPassword(string password): void |
| `roles` | `string[]` | Required | List of [roles](https://docs.adyen.com/development-resources/api-credentials#roles-1) for the API credential. | getRoles(): array | setRoles(array roles): void |
| `username` | `string` | Required | The name of the [API credential](https://docs.adyen.com/development-resources/api-credentials), for example **ws@Company.TestCompany**. | getUsername(): string | setUsername(string username): void |

## Example (as JSON)

```json
{
  "_links": {
    "allowedOrigins": {
      "href": "href6"
    },
    "company": {
      "href": "href2"
    },
    "generateApiKey": {
      "href": "href6"
    },
    "generateClientKey": {
      "href": "href4"
    },
    "merchant": {
      "href": "href6"
    },
    "self": {
      "href": "href0"
    }
  },
  "active": false,
  "allowedIpAddresses": [
    "allowedIpAddresses7"
  ],
  "allowedOrigins": [
    {
      "_links": {
        "self": {
          "href": "href0"
        }
      },
      "domain": "domain0",
      "id": "id4"
    }
  ],
  "apiKey": "apiKey8",
  "associatedMerchantAccounts": [
    "associatedMerchantAccounts8",
    "associatedMerchantAccounts9",
    "associatedMerchantAccounts0"
  ],
  "clientKey": "clientKey8",
  "description": "description2",
  "id": "id8",
  "password": "password2",
  "roles": [
    "roles8"
  ],
  "username": "username2"
}
```

