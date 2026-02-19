
# Bill Desk

## Structure

`BillDesk`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `string` | Required | The issuer id of the shopper's selected bank. | getIssuer(): string | setIssuer(string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`string(Type10)`](../../doc/models/type-10.md) | Required | **billdesk** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId6",
  "issuer": "issuer0",
  "sdkData": "sdkData0",
  "type": "billdesk_online"
}
```

