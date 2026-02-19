
# Givex Info 1

Details to provide if `type` is **givex**.

## Structure

`GivexInfo1`

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
  "currencyCode": "currencyCode0",
  "password": "password4",
  "paymentFlow": "Ecommerce",
  "username": "username0"
}
```

