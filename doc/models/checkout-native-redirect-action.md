
# Checkout Native Redirect Action

## Structure

`CheckoutNativeRedirectAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | `?array<string,string>` | Optional | When the redirect URL must be accessed via POST, use this data to post to the redirect URL. | getData(): ?array | setData(?array data): void |
| `method` | `?string` | Optional | Specifies the HTTP method, for example GET or POST. | getMethod(): ?string | setMethod(?string method): void |
| `nativeRedirectData` | `?string` | Optional | Native SDK's redirect data containing the direct issuer link and state data that must be submitted to the /v1/nativeRedirect/redirectResult. | getNativeRedirectData(): ?string | setNativeRedirectData(?string nativeRedirectData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `type` | `string` | Required, Constant | **nativeRedirect**<br><br>**Value**: `'nativeRedirect'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "nativeRedirect",
  "data": {
    "key0": "data5"
  },
  "method": "method6",
  "nativeRedirectData": "nativeRedirectData8",
  "paymentMethodType": "paymentMethodType2",
  "url": "url4"
}
```

