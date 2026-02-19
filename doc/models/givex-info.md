
# Givex Info

## Structure

`GivexInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currencyCode` | `string` | Required | The three-character ISO currency code, such as **EUR**. | getCurrencyCode(): string | setCurrencyCode(string currencyCode): void |
| `password` | `string` | Required | The password provided by the acquirer. | getPassword(): string | setPassword(string password): void |
| `paymentFlow` | [`string(PaymentFlow)`](../../doc/models/payment-flow.md) | Required | The sales channel used for the payment. | getPaymentFlow(): string | setPaymentFlow(string paymentFlow): void |
| `username` | `string` | Required | The username provided by the acquirer. | getUsername(): string | setUsername(string username): void |

## Example (as JSON)

```json
{
  "currencyCode": "currencyCode2",
  "password": "password6",
  "paymentFlow": "Ecommerce",
  "username": "username8"
}
```

