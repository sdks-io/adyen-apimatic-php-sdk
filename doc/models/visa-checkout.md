
# Visa Checkout

*This model accepts additional fields of type array.*

## Structure

`VisaCheckout`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `fundingSource` | [`?string(FundingSource)`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type49)`](../../doc/models/type-49.md) | Optional | **visacheckout**<br><br>**Default**: `Type49::VISACHECKOUT` | getType(): ?string | setType(?string type): void |
| `visaCheckoutCallId` | `string` | Required | The Visa Click to Pay Call ID value. When your shopper selects a payment and/or a shipping address from Visa Click to Pay, you will receive a Visa Click to Pay Call ID. | getVisaCheckoutCallId(): string | setVisaCheckoutCallId(string visaCheckoutCallId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "visacheckout",
  "visaCheckoutCallId": "visaCheckoutCallId0",
  "checkoutAttemptId": "checkoutAttemptId8",
  "fundingSource": "credit",
  "sdkData": "sdkData8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

