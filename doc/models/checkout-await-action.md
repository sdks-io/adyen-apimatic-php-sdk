
# Checkout Await Action

## Structure

`CheckoutAwaitAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `paymentData` | `?string` | Optional | Encoded payment data. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `type` | `string` | Required, Constant | **await**<br><br>**Value**: `'await'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "await",
  "paymentData": "paymentData8",
  "paymentMethodType": "paymentMethodType8",
  "url": "url0"
}
```

