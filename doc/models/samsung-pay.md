
# Samsung Pay

*This model accepts additional fields of type array.*

## Structure

`SamsungPay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `fundingSource` | [`?string(FundingSource)`](../../doc/models/funding-source.md) | Optional | The funding source that should be used when multiple sources are available. For Brazilian combo cards, by default the funding source is credit. To use debit, set this value to **debit**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `samsungPayToken` | `string` | Required | The payload you received from the Samsung Pay SDK response.<br><br>**Constraints**: *Maximum Length*: `10000` | getSamsungPayToken(): string | setSamsungPayToken(string samsungPayToken): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type44)`](../../doc/models/type-44.md) | Optional | **samsungpay**<br><br>**Default**: `Type44::SAMSUNGPAY` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "samsungPayToken": "samsungPayToken6",
  "type": "samsungpay",
  "checkoutAttemptId": "checkoutAttemptId4",
  "fundingSource": "prepaid",
  "recurringDetailReference": "recurringDetailReference8",
  "sdkData": "sdkData2",
  "storedPaymentMethodId": "storedPaymentMethodId2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

