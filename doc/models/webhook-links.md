
# Webhook Links

## Structure

`WebhookLinks`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `company` | [`?LinksElement15`](../../doc/models/links-element-15.md) | Optional | The company account that the webhook is configured for. Only present for company-level webhooks. | getCompany(): ?LinksElement15 | setCompany(?LinksElement15 company): void |
| `generateHmac` | [`LinksElement16`](../../doc/models/links-element-16.md) | Required | Generate an HMAC key. | getGenerateHmac(): LinksElement16 | setGenerateHmac(LinksElement16 generateHmac): void |
| `merchant` | [`?LinksElement17`](../../doc/models/links-element-17.md) | Optional | The merchant account that the webhook is configured for. Only present for merchant-level webhooks. | getMerchant(): ?LinksElement17 | setMerchant(?LinksElement17 merchant): void |
| `self` | [`LinksElement6`](../../doc/models/links-element-6.md) | Required | Link to the resource itself. | getSelf(): LinksElement6 | setSelf(LinksElement6 self): void |
| `testWebhook` | [`LinksElement19`](../../doc/models/links-element-19.md) | Required | Test the webhook setup. | getTestWebhook(): LinksElement19 | setTestWebhook(LinksElement19 testWebhook): void |

## Example (as JSON)

```json
{
  "company": {
    "href": "href2"
  },
  "generateHmac": {
    "href": "href6"
  },
  "merchant": {
    "href": "href6"
  },
  "self": {
    "href": "href0"
  },
  "testWebhook": {
    "href": "href6"
  }
}
```

