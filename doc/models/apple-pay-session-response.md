
# Apple Pay Session Response

## Structure

`ApplePaySessionResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | `string` | Required | Base64 encoded data you need to [complete the Apple Pay merchant validation](https://docs.adyen.com/payment-methods/apple-pay/api-only?tab=adyen-certificate-validation_1#complete-apple-pay-session-validation). | getData(): string | setData(string data): void |

## Example (as JSON)

```json
{
  "data": "data4"
}
```

