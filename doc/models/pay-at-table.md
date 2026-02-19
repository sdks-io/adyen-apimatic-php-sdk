
# Pay at Table

## Structure

`PayAtTable`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authenticationMethod` | [`?string(AuthenticationMethod)`](../../doc/models/authentication-method.md) | Optional | Allowed authentication methods: Magswipe, Manual Entry. | getAuthenticationMethod(): ?string | setAuthenticationMethod(?string authenticationMethod): void |
| `enablePayAtTable` | `?bool` | Optional | Enable Pay at table. | getEnablePayAtTable(): ?bool | setEnablePayAtTable(?bool enablePayAtTable): void |
| `paymentInstrument` | [`?string(PaymentInstrument)`](../../doc/models/payment-instrument.md) | Optional | Sets the allowed payment instrument for Pay at table transactions.  Can be: **cash** or **card**. If not set, the terminal presents both options. | getPaymentInstrument(): ?string | setPaymentInstrument(?string paymentInstrument): void |

## Example (as JSON)

```json
{
  "authenticationMethod": "MAGSWIPE",
  "enablePayAtTable": false,
  "paymentInstrument": "Cash"
}
```

