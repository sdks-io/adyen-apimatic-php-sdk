
# Standalone Payment Cancel Response

## Structure

`StandalonePaymentCancelResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantAccount` | `string` | Required | The merchant account that is used to process the payment. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `paymentReference` | `string` | Required | The [`reference`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments__reqParam_reference) of the payment to cancel. | getPaymentReference(): string | setPaymentReference(string paymentReference): void |
| `pspReference` | `string` | Required | Adyen's 16-character reference associated with the cancel request. | getPspReference(): string | setPspReference(string pspReference): void |
| `reference` | `?string` | Optional | Your reference for the cancel request. | getReference(): ?string | setReference(?string reference): void |
| `status` | `string` | Required, Constant | The status of your request. This will always have the value **received**.<br><br>**Value**: `'received'` | getStatus(): string | setStatus(string status): void |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount6",
  "paymentReference": "paymentReference2",
  "pspReference": "pspReference6",
  "status": "received",
  "reference": "reference2"
}
```

