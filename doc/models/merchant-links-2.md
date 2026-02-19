
# Merchant Links 2

References to resources connected with this merchant.

## Structure

`MerchantLinks2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiCredentials` | [`?LinksElement`](../../doc/models/links-element.md) | Optional | - | getApiCredentials(): ?LinksElement | setApiCredentials(?LinksElement apiCredentials): void |
| `self` | [`LinksElement6`](../../doc/models/links-element-6.md) | Required | Link to the resource itself. | getSelf(): LinksElement6 | setSelf(LinksElement6 self): void |
| `users` | [`?LinksElement`](../../doc/models/links-element.md) | Optional | - | getUsers(): ?LinksElement | setUsers(?LinksElement users): void |
| `webhooks` | [`?LinksElement`](../../doc/models/links-element.md) | Optional | - | getWebhooks(): ?LinksElement | setWebhooks(?LinksElement webhooks): void |

## Example (as JSON)

```json
{
  "apiCredentials": {
    "href": "href8"
  },
  "self": {
    "href": "href0"
  },
  "users": {
    "href": "href8"
  },
  "webhooks": {
    "href": "href8"
  }
}
```

