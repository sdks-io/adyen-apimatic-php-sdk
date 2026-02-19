
# Cellulant

## Structure

`Cellulant`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `?string` | Optional | The Cellulant issuer. | getIssuer(): ?string | setIssuer(?string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type15)`](../../doc/models/type-15.md) | Optional | **Cellulant**<br><br>**Default**: `Type15::CELLULANT` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "cellulant",
  "checkoutAttemptId": "checkoutAttemptId0",
  "issuer": "issuer4",
  "sdkData": "sdkData6"
}
```

