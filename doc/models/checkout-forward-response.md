
# Checkout Forward Response

## Structure

`CheckoutForwardResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantReference` | `?string` | Optional | Merchant defined payment reference. | getMerchantReference(): ?string | setMerchantReference(?string merchantReference): void |
| `pspReference` | `?string` | Optional | Adyen's 16-character reference associated with the transaction/request. This value is globally unique. Use this reference when you communicate with us about this request. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `response` | [`CheckoutForwardResponseFromUrl2`](../../doc/models/checkout-forward-response-from-url-2.md) | Required | The details of the response Adyen received from the third party. | getResponse(): CheckoutForwardResponseFromUrl2 | setResponse(CheckoutForwardResponseFromUrl2 response): void |
| `storedPaymentMethodId` | `?string` | Optional | The unique identifier of the token. | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |

## Example (as JSON)

```json
{
  "merchantReference": "merchantReference4",
  "pspReference": "pspReference6",
  "response": {
    "body": "body6",
    "headers": {
      "key0": "headers3",
      "key1": "headers4",
      "key2": "headers5"
    },
    "status": 110
  },
  "storedPaymentMethodId": "storedPaymentMethodId6"
}
```

