
# E Banking Finland

## Structure

`EBankingFinland`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `?string` | Optional | The Ebanking Finland issuer value of the shopper's selected bank. | getIssuer(): ?string | setIssuer(?string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | `string` | Required, Constant | **ebanking_FI**<br><br>**Value**: `'ebanking_FI'` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "type": "ebanking_FI",
  "checkoutAttemptId": "checkoutAttemptId4",
  "issuer": "issuer8",
  "sdkData": "sdkData2"
}
```

