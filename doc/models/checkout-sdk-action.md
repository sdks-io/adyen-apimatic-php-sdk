
# Checkout Sdk Action

## Structure

`CheckoutSdkAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `paymentData` | `?string` | Optional | Encoded payment data. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `sdkData` | `?array<string,string>` | Optional | The data to pass to the SDK. | getSdkData(): ?array | setSdkData(?array sdkData): void |
| `type` | [`string(Type17)`](../../doc/models/type-17.md) | Required | The type of the action. | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "paymentData": "paymentData4",
  "paymentMethodType": "paymentMethodType4",
  "sdkData": {
    "key0": "sdkData3",
    "key1": "sdkData4"
  },
  "type": "sdk",
  "url": "url6"
}
```

