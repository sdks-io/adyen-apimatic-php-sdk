
# Apple Pay Info

## Structure

`ApplePayInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `domains` | `string[]` | Required | The list of merchant domains. Maximum: 99 domains per request.<br><br>For more information, see [Apple Pay documentation](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in?tab=adyen-certificate-live_1#going-live). | getDomains(): array | setDomains(array domains): void |

## Example (as JSON)

```json
{
  "domains": [
    "domains4"
  ]
}
```

