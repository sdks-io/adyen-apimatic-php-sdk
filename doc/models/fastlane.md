
# Fastlane

## Structure

`Fastlane`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `fastlaneData` | `string` | Required | The encoded fastlane data blob | getFastlaneData(): string | setFastlaneData(string fastlaneData): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | `string` | Required, Constant | **fastlane**<br><br>**Value**: `'fastlane'` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "fastlaneData": "fastlaneData2",
  "type": "fastlane",
  "checkoutAttemptId": "checkoutAttemptId4",
  "recurringDetailReference": "recurringDetailReference8",
  "sdkData": "sdkData2",
  "storedPaymentMethodId": "storedPaymentMethodId2"
}
```

