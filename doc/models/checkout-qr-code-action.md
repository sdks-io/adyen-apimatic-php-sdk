
# Checkout Qr Code Action

## Structure

`CheckoutQrCodeAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `expiresAt` | `?string` | Optional | Expiry time of the QR code. | getExpiresAt(): ?string | setExpiresAt(?string expiresAt): void |
| `paymentData` | `?string` | Optional | Encoded payment data. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `qrCodeData` | `?string` | Optional | The contents of the QR code as a UTF8 string. | getQrCodeData(): ?string | setQrCodeData(?string qrCodeData): void |
| `type` | `string` | Required, Constant | **qrCode**<br><br>**Value**: `'qrCode'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "qrCode",
  "expiresAt": "expiresAt8",
  "paymentData": "paymentData4",
  "paymentMethodType": "paymentMethodType4",
  "qrCodeData": "qrCodeData4",
  "url": "url6"
}
```

