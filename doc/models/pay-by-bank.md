
# Pay by Bank

## Structure

`PayByBank`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `?string` | Optional | The PayByBank issuer value of the shopper's selected bank. | getIssuer(): ?string | setIssuer(?string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | `string` | Required, Constant | **paybybank**<br><br>**Value**: `'paybybank'` | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "type": "paybybank",
  "checkoutAttemptId": "checkoutAttemptId2",
  "issuer": "issuer6",
  "sdkData": "sdkData4"
}
```

