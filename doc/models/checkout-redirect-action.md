
# Checkout Redirect Action

## Structure

`CheckoutRedirectAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | `?array<string,string>` | Optional | When the redirect URL must be accessed via POST, use this data to post to the redirect URL. | getData(): ?array | setData(?array data): void |
| `method` | `?string` | Optional | Specifies the HTTP method, for example GET or POST. | getMethod(): ?string | setMethod(?string method): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `type` | `string` | Required, Constant | **redirect**<br><br>**Value**: `'redirect'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "redirect",
  "data": {
    "key0": "data5",
    "key1": "data6",
    "key2": "data7"
  },
  "method": "method4",
  "paymentMethodType": "paymentMethodType2",
  "url": "url4"
}
```

