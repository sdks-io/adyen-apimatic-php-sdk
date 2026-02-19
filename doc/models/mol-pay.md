
# Mol Pay

## Structure

`MolPay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `string` | Required | The shopper's bank. Specify this with the issuer value that corresponds to this bank. | getIssuer(): string | setIssuer(string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`string(Type33)`](../../doc/models/type-33.md) | Required | **molpay** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId6",
  "issuer": "issuer0",
  "sdkData": "sdkData0",
  "type": "molpay_ebanking_fpx_MY"
}
```

