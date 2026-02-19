
# Checkout Delegated Authentication Action

## Structure

`CheckoutDelegatedAuthenticationAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authorisationToken` | `?string` | Optional | A token needed to authorise a payment. | getAuthorisationToken(): ?string | setAuthorisationToken(?string authorisationToken): void |
| `paymentData` | `?string` | Optional | Encoded payment data. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `token` | `?string` | Optional | A token to pass to the delegatedAuthentication component. | getToken(): ?string | setToken(?string token): void |
| `type` | `string` | Required, Constant | **delegatedAuthentication**<br><br>**Value**: `'delegatedAuthentication'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "delegatedAuthentication",
  "authorisationToken": "authorisationToken4",
  "paymentData": "paymentData2",
  "paymentMethodType": "paymentMethodType2",
  "token": "token4",
  "url": "url4"
}
```

