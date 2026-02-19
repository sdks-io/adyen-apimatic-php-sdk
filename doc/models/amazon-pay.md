
# Amazon Pay

## Structure

`AmazonPay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amazonPayToken` | `?string` | Optional | This is the `amazonPayToken` that you obtained from the [Get Checkout Session](https://amazon-pay-acquirer-guide.s3-eu-west-1.amazonaws.com/v1/amazon-pay-api-v2/checkout-session.html#get-checkout-session) response. This token is used for API only integration specifically. | getAmazonPayToken(): ?string | setAmazonPayToken(?string amazonPayToken): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `checkoutSessionId` | `?string` | Optional | The `checkoutSessionId` is used to identify the checkout session at the Amazon Pay side. This field is required only for drop-in and components integration, where it replaces the amazonPayToken. | getCheckoutSessionId(): ?string | setCheckoutSessionId(?string checkoutSessionId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type3)`](../../doc/models/type-3.md) | Optional | **amazonpay**<br><br>**Default**: `Type3::AMAZONPAY` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "amazonpay",
  "amazonPayToken": "amazonPayToken4",
  "checkoutAttemptId": "checkoutAttemptId2",
  "checkoutSessionId": "checkoutSessionId4",
  "sdkData": "sdkData4"
}
```

