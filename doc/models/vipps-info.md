
# Vipps Info

## Structure

`VippsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `logo` | `string` | Required | Vipps logo. Format: Base64-encoded string. | getLogo(): string | setLogo(string logo): void |
| `subscriptionCancelUrl` | `?string` | Optional | Vipps subscription cancel url (required in case of [recurring payments](https://docs.adyen.com/online-payments/tokenization)) | getSubscriptionCancelUrl(): ?string | setSubscriptionCancelUrl(?string subscriptionCancelUrl): void |

## Example (as JSON)

```json
{
  "logo": "logo8",
  "subscriptionCancelUrl": "subscriptionCancelUrl0"
}
```

