
# Affirm

## Structure

`Affirm`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type1)`](../../doc/models/type-1.md) | Optional | **affirm**<br><br>**Default**: `Type1::AFFIRM` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "affirm",
  "checkoutAttemptId": "checkoutAttemptId6",
  "sdkData": "sdkData0"
}
```

