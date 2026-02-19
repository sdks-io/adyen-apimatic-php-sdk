
# Vipps Info 1

Details to provide if `type` is **vipps**.

## Structure

`VippsInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `logo` | `string` | Required | Vipps logo. Format: Base64-encoded string. | getLogo(): string | setLogo(string logo): void |
| `subscriptionCancelUrl` | `?string` | Optional | Vipps subscription cancel url (required in case of [recurring payments](https://docs.adyen.com/online-payments/tokenization)) | getSubscriptionCancelUrl(): ?string | setSubscriptionCancelUrl(?string subscriptionCancelUrl): void |

## Example (as JSON)

```json
{
  "logo": "logo6",
  "subscriptionCancelUrl": "subscriptionCancelUrl4"
}
```

