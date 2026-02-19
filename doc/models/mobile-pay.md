
# Mobile Pay

## Structure

`MobilePay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type32)`](../../doc/models/type-32.md) | Optional | **mobilepay**<br><br>**Default**: `Type32::MOBILEPAY` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "mobilepay",
  "checkoutAttemptId": "checkoutAttemptId0",
  "sdkData": "sdkData6"
}
```

