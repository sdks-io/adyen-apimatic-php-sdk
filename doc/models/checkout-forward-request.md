
# Checkout Forward Request

## Structure

`CheckoutForwardRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `baseUrl` | `string` | Required | The base URL of the third party API, where Adyen will send the request to forward the payment details. | getBaseUrl(): string | setBaseUrl(string baseUrl): void |
| `merchantAccount` | `string` | Required | Your merchant account. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `merchantReference` | `?string` | Optional | Merchant defined payment reference. | getMerchantReference(): ?string | setMerchantReference(?string merchantReference): void |
| `options` | [`?CheckoutForwardRequestOptions2`](../../doc/models/checkout-forward-request-options-2.md) | Optional | The customizations that can be applied when making a forward request. | getOptions(): ?CheckoutForwardRequestOptions2 | setOptions(?CheckoutForwardRequestOptions2 options): void |
| `paymentMethod` | [`?CheckoutForwardRequestCard2`](../../doc/models/checkout-forward-request-card-2.md) | Optional | The card details. | getPaymentMethod(): ?CheckoutForwardRequestCard2 | setPaymentMethod(?CheckoutForwardRequestCard2 paymentMethod): void |
| `request` | [`CheckoutOutgoingForwardRequest2`](../../doc/models/checkout-outgoing-forward-request-2.md) | Required | The [details of the request](https://docs.adyen.com/online-payments/tokenization/forward-payment-details#request-to-adyen-card) that you want to forward to the third-party. | getRequest(): CheckoutOutgoingForwardRequest2 | setRequest(CheckoutOutgoingForwardRequest2 request): void |
| `shopperReference` | `string` | Required | Your reference to uniquely identify this shopper, for example user ID or account ID. The value is case-sensitive and must be at least three characters.<br><br>> Your reference must not include personally identifiable information (PII) such as name or email address. | getShopperReference(): string | setShopperReference(string shopperReference): void |
| `storedPaymentMethodId` | `?string` | Optional | The unique identifier of the token that you want to forward to the third party. This is the `storedPaymentMethodId` you received in the webhook after you created the token. | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |

## Example (as JSON)

```json
{
  "baseUrl": "baseUrl6",
  "merchantAccount": "merchantAccount0",
  "merchantReference": "merchantReference2",
  "options": {
    "accountUpdate": false,
    "dryRun": false,
    "networkToken": {
      "includeCryptogram": false,
      "useNetworkToken": false
    },
    "networkTxReferencePaths": [
      "networkTxReferencePaths7"
    ],
    "tokenize": false
  },
  "paymentMethod": {
    "cvc": "cvc6",
    "encryptedCardNumber": "encryptedCardNumber0",
    "encryptedExpiryMonth": "encryptedExpiryMonth2",
    "encryptedExpiryYear": "encryptedExpiryYear2",
    "encryptedSecurityCode": "encryptedSecurityCode2"
  },
  "request": {
    "body": "body2",
    "credentials": "credentials0",
    "headers": {
      "key0": "headers9"
    },
    "httpMethod": "post",
    "urlSuffix": "urlSuffix2"
  },
  "shopperReference": "shopperReference6",
  "storedPaymentMethodId": "storedPaymentMethodId2"
}
```

