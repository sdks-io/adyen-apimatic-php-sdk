
# Payment Response 9

Action to be taken for completing the payment.

## Structure

`PaymentResponse9`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [CheckoutAwaitAction](../../doc/models/checkout-await-action.md)\|[CheckoutBankTransferAction](../../doc/models/checkout-bank-transfer-action.md)\|[CheckoutDelegatedAuthenticationAction](../../doc/models/checkout-delegated-authentication-action.md)\|[CheckoutNativeRedirectAction](../../doc/models/checkout-native-redirect-action.md)\|[CheckoutQrCodeAction](../../doc/models/checkout-qr-code-action.md)\|[CheckoutRedirectAction](../../doc/models/checkout-redirect-action.md)\|[CheckoutSdkAction](../../doc/models/checkout-sdk-action.md)\|[CheckoutThreeDs2Action](../../doc/models/checkout-three-ds-2-action.md)\|Checkout[Voucher](../../doc/models/voucher.md)Action\|null | Optional | This is a container for one-of cases. | getAction(): | setAction( action): void |
| `additionalData` | `?array<string,string>` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first: Go to **Customer Area** > **Developers** > **Additional data**. | getAdditionalData(): ?array | setAdditionalData(?array additionalData): void |
| `amount` | [`?Amount25`](../../doc/models/amount-25.md) | Optional | Authorised amount in the transaction. | getAmount(): ?Amount25 | setAmount(?Amount25 amount): void |
| `donationToken` | `?string` | Optional | Donation Token containing payment details for Adyen Giving. | getDonationToken(): ?string | setDonationToken(?string donationToken): void |
| `fraudResult` | [`?FraudResult1`](../../doc/models/fraud-result-1.md) | Optional | The fraud result properties of the payment. | getFraudResult(): ?FraudResult1 | setFraudResult(?FraudResult1 fraudResult): void |
| `merchantReference` | `?string` | Optional | The reference to uniquely identify a payment. This reference is used in all communication with you about the payment status. We recommend using a unique value per payment; however, it is not a requirement.<br>If you need to provide multiple references for a transaction, separate them with hyphens ("-").<br>Maximum length: 80 characters. | getMerchantReference(): ?string | setMerchantReference(?string merchantReference): void |
| `order` | [`?CheckoutOrderResponse1`](../../doc/models/checkout-order-response-1.md) | Optional | Contains updated information regarding the order in case order information was provided in the request. | getOrder(): ?CheckoutOrderResponse1 | setOrder(?CheckoutOrderResponse1 order): void |
| `paymentMethod` | [`?PaymentResponse1`](../../doc/models/payment-response-1.md) | Optional | Details about the payment method used in the transaction.<br>Only returned if `resultCode` is **Authorised**. | getPaymentMethod(): ?PaymentResponse1 | setPaymentMethod(?PaymentResponse1 paymentMethod): void |
| `paymentValidations` | [`?PaymentResponse2`](../../doc/models/payment-response-2.md) | Optional | The object that contains the validation outcomes.<br>Only returned if `resultCode` is **Authorised** and if you have requested a payment validation in the request. | getPaymentValidations(): ?PaymentResponse2 | setPaymentValidations(?PaymentResponse2 paymentValidations): void |
| `pspReference` | `?string` | Optional | Adyen's 16-character string reference associated with the transaction/request. This value is globally unique; quote it when communicating with us about this request.<br><br>> For payment methods that require a redirect or additional action, you will get this value in the `/payments/details` response. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `refusalReason` | `?string` | Optional | If the payment's authorisation is refused or an error occurs during authorisation, this field holds Adyen's mapped reason for the refusal or a description of the error. When a transaction fails, the authorisation response includes `resultCode` and `refusalReason` values.<br><br>For more information, see [Refusal reasons](https://docs.adyen.com/development-resources/refusal-reasons). | getRefusalReason(): ?string | setRefusalReason(?string refusalReason): void |
| `refusalReasonCode` | `?string` | Optional | Code that specifies the refusal reason. For more information, see [Authorisation refusal reasons](https://docs.adyen.com/development-resources/refusal-reasons). | getRefusalReasonCode(): ?string | setRefusalReasonCode(?string refusalReasonCode): void |
| `resultCode` | [`?string(ResultCode1)`](../../doc/models/result-code-1.md) | Optional | The result of the payment. For more information, see [Result codes](https://docs.adyen.com/online-payments/payment-result-codes).<br><br>Possible values:<br><br>* **AuthenticationFinished** – The payment has been successfully authenticated with 3D Secure 2. Returned for 3D Secure 2 authentication-only transactions.<br>* **AuthenticationNotRequired** – The transaction does not require 3D Secure authentication. Returned for [standalone authentication-only integrations](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only).<br>* **Authorised** – The payment was successfully authorised. This state serves as an indicator to proceed with the delivery of goods and services. This is a final state.<br>* **Cancelled** – Indicates the payment has been cancelled (either by the shopper or the merchant) before processing was completed. This is a final state.<br>* **ChallengeShopper** – The issuer requires further shopper interaction before the payment can be authenticated. Returned for 3D Secure 2 transactions.<br>* **Error** – There was an error when the payment was being processed. The reason is given in the `refusalReason` field. This is a final state.<br>* **IdentifyShopper** – The issuer requires the shopper's device fingerprint before the payment can be authenticated. Returned for 3D Secure 2 transactions.<br>* **PartiallyAuthorised** – The payment has been authorised for a partial amount.<br>  This happens for card payments when the merchant supports Partial Authorisations and the cardholder has insufficient funds.<br>* **Pending** – Indicates that it is not possible to obtain the final status of the payment. This can happen if the systems providing final status information for the payment are unavailable, or if the shopper needs to take further action to complete the payment.<br>* **PresentToShopper** – Indicates that the response contains additional information that you need to present to a shopper, so that they can use it to complete a payment.<br>* **Received** – Indicates the payment has successfully been received by Adyen, and will be processed. This is the initial state for all payments.<br>* **RedirectShopper** – Indicates the shopper should be redirected to an external web page or app to complete the authorisation.<br>* **Refused** – Indicates the payment was refused. The reason is given in the `refusalReason` field. This is a final state. | getResultCode(): ?string | setResultCode(?string resultCode): void |
| `threeDs2ResponseData` | [`?ThreeDs2ResponseData1`](../../doc/models/three-ds-2-response-data-1.md) | Optional | Response of the 3D Secure 2 authentication. | getThreeDs2ResponseData(): ?ThreeDs2ResponseData1 | setThreeDs2ResponseData(?ThreeDs2ResponseData1 threeDs2ResponseData): void |
| `threeDs2Result` | [`?ThreeDs2Result1`](../../doc/models/three-ds-2-result-1.md) | Optional | Result of the 3D Secure 2 authentication. | getThreeDs2Result(): ?ThreeDs2Result1 | setThreeDs2Result(?ThreeDs2Result1 threeDs2Result): void |
| `threeDsPaymentData` | `?string` | Optional | When non-empty, contains a value that you must submit to the `/payments/details` endpoint as `paymentData`. | getThreeDsPaymentData(): ?string | setThreeDsPaymentData(?string threeDsPaymentData): void |

## Example (as JSON)

```json
{
  "action": {
    "paymentData": "paymentData8",
    "paymentMethodType": "paymentMethodType8",
    "type": "type4",
    "url": "url0"
  },
  "additionalData": {
    "key0": "additionalData6"
  },
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "donationToken": "donationToken8",
  "fraudResult": {
    "accountScore": 232,
    "results": [
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      },
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      }
    ]
  }
}
```

