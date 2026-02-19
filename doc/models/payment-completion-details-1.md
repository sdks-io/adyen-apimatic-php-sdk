
# Payment Completion Details 1

Use this collection to submit the details that were returned as a result of the `/payments` call.

## Structure

`PaymentCompletionDetails1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `md` | `?string` | Optional | A payment session identifier returned by the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` | getMd(): ?string | setMd(?string md): void |
| `paReq` | `?string` | Optional | (3D) Payment Authentication Request data for the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` | getPaReq(): ?string | setPaReq(?string paReq): void |
| `paRes` | `?string` | Optional | (3D) Payment Authentication Response data by the card issuer.<br><br>**Constraints**: *Maximum Length*: `20000` | getPaRes(): ?string | setPaRes(?string paRes): void |
| `authorizationToken` | `?string` | Optional | - | getAuthorizationToken(): ?string | setAuthorizationToken(?string authorizationToken): void |
| `billingToken` | `?string` | Optional | PayPal-generated token for recurring payments. | getBillingToken(): ?string | setBillingToken(?string billingToken): void |
| `cupsecureplusSmscode` | `?string` | Optional | The SMS verification code collected from the shopper. | getCupsecureplusSmscode(): ?string | setCupsecureplusSmscode(?string cupsecureplusSmscode): void |
| `facilitatorAccessToken` | `?string` | Optional | PayPal-generated third party access token. | getFacilitatorAccessToken(): ?string | setFacilitatorAccessToken(?string facilitatorAccessToken): void |
| `oneTimePasscode` | `?string` | Optional | A random number sent to the mobile phone number of the shopper to verify the payment. | getOneTimePasscode(): ?string | setOneTimePasscode(?string oneTimePasscode): void |
| `orderId` | `?string` | Optional | PayPal-assigned ID for the order. | getOrderId(): ?string | setOrderId(?string orderId): void |
| `payerId` | `?string` | Optional | PayPal-assigned ID for the payer (shopper). | getPayerId(): ?string | setPayerId(?string payerId): void |
| `payload` | `?string` | Optional | Payload appended to the `returnURL` as a result of the redirect.<br><br>**Constraints**: *Maximum Length*: `20000` | getPayload(): ?string | setPayload(?string payload): void |
| `paymentId` | `?string` | Optional | PayPal-generated ID for the payment. | getPaymentId(): ?string | setPaymentId(?string paymentId): void |
| `paymentStatus` | `?string` | Optional | Value passed from the WeChat MiniProgram `wx.requestPayment` **complete** callback. Possible values: any value starting with `requestPayment:`. | getPaymentStatus(): ?string | setPaymentStatus(?string paymentStatus): void |
| `redirectResult` | `?string` | Optional | The result of the redirect as appended to the `returnURL`.<br><br>**Constraints**: *Maximum Length*: `20000` | getRedirectResult(): ?string | setRedirectResult(?string redirectResult): void |
| `resultCode` | `?string` | Optional | Value you received from the WeChat Pay SDK. | getResultCode(): ?string | setResultCode(?string resultCode): void |
| `returnUrlQueryString` | `?string` | Optional | The query string as appended to the `returnURL` when using direct issuer links .<br><br>**Constraints**: *Maximum Length*: `20000` | getReturnUrlQueryString(): ?string | setReturnUrlQueryString(?string returnUrlQueryString): void |
| `threeDsResult` | `?string` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameters: `transStatus`, `authorisationToken`.<br><br>**Constraints**: *Maximum Length*: `50000` | getThreeDsResult(): ?string | setThreeDsResult(?string threeDsResult): void |
| `threeds2ChallengeResult` | `?string` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameter: `transStatus`.<br><br>**Constraints**: *Maximum Length*: `50000` | getThreeds2ChallengeResult(): ?string | setThreeds2ChallengeResult(?string threeds2ChallengeResult): void |
| `threeds2Fingerprint` | `?string` | Optional | Base64-encoded string returned by the Component after the challenge flow. It contains the following parameter: `threeDSCompInd`.<br><br>**Constraints**: *Maximum Length*: `100000` | getThreeds2Fingerprint(): ?string | setThreeds2Fingerprint(?string threeds2Fingerprint): void |
| `vaultToken` | `?string` | Optional | PayPalv2-generated token for recurring payments. | getVaultToken(): ?string | setVaultToken(?string vaultToken): void |

## Example (as JSON)

```json
{
  "MD": "MD8",
  "PaReq": "PaReq4",
  "PaRes": "PaRes4",
  "authorization_token": "authorization_token8",
  "billingToken": "billingToken6"
}
```

