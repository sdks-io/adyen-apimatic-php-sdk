
# Mb Way

## Structure

`MbWay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperEmail` | `string` | Required | - | getShopperEmail(): string | setShopperEmail(string shopperEmail): void |
| `telephoneNumber` | `string` | Required | - | getTelephoneNumber(): string | setTelephoneNumber(string telephoneNumber): void |
| `type` | [`?string(Type31)`](../../doc/models/type-31.md) | Optional | **mbway**<br><br>**Default**: `Type31::MBWAY` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "shopperEmail": "shopperEmail4",
  "telephoneNumber": "telephoneNumber4",
  "type": "mbway",
  "checkoutAttemptId": "checkoutAttemptId8",
  "sdkData": "sdkData8"
}
```

