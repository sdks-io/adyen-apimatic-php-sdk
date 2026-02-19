
# Masterpass

## Structure

`Masterpass`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `fundingSource` | [`?string(FundingSource)`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `masterpassTransactionId` | `string` | Required | The Masterpass transaction ID. | getMasterpassTransactionId(): string | setMasterpassTransactionId(string masterpassTransactionId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type30)`](../../doc/models/type-30.md) | Optional | **masterpass**<br><br>**Default**: `Type30::MASTERPASS` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "masterpassTransactionId": "masterpassTransactionId0",
  "type": "masterpass",
  "checkoutAttemptId": "checkoutAttemptId4",
  "fundingSource": "credit",
  "sdkData": "sdkData2"
}
```

