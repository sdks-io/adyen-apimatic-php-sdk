
# Payment Cancel Response

## Structure

`PaymentCancelResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantAccount` | `string` | Required | The merchant account that is used to process the payment. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `paymentPspReference` | `string` | Required | The [`pspReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-pspReference) of the payment to cancel. | getPaymentPspReference(): string | setPaymentPspReference(string paymentPspReference): void |
| `pspReference` | `string` | Required | Adyen's 16-character reference associated with the cancel request. | getPspReference(): string | setPspReference(string pspReference): void |
| `reference` | `?string` | Optional | Your reference for the cancel request. | getReference(): ?string | setReference(?string reference): void |
| `status` | `string` | Required, Constant | The status of your request. This will always have the value **received**.<br><br>**Value**: `'received'` | getStatus(): string | setStatus(string status): void |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount2",
  "paymentPspReference": "paymentPspReference8",
  "pspReference": "pspReference2",
  "status": "received",
  "reference": "reference6"
}
```

