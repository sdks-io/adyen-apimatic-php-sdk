
# Google Pay 2

## Structure

`GooglePay2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `fundingSource` | [`?string(FundingSource)`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `googlePayCardNetwork` | `?string` | Optional | The selected payment card network. | getGooglePayCardNetwork(): ?string | setGooglePayCardNetwork(?string googlePayCardNetwork): void |
| `googlePayToken` | `string` | Required | The `token` that you obtained from the [Google Pay API](https://developers.google.com/pay/api/web/reference/response-objects#PaymentData) `PaymentData` response.<br><br>**Constraints**: *Maximum Length*: `10000` | getGooglePayToken(): string | setGooglePayToken(string googlePayToken): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `threeDs2SdkVersion` | `?string` | Optional | Required for mobile integrations. Version of the 3D Secure 2 mobile SDK.<br><br>**Constraints**: *Maximum Length*: `12` | getThreeDs2SdkVersion(): ?string | setThreeDs2SdkVersion(?string threeDs2SdkVersion): void |
| `type` | [`?string(Type20)`](../../doc/models/type-20.md) | Optional | **googlepay**, **paywithgoogle**<br><br>**Default**: `Type20::GOOGLEPAY` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "googlePayToken": "googlePayToken6",
  "type": "googlepay",
  "checkoutAttemptId": "checkoutAttemptId0",
  "fundingSource": "credit",
  "googlePayCardNetwork": "googlePayCardNetwork0",
  "recurringDetailReference": "recurringDetailReference4",
  "sdkData": "sdkData6"
}
```

