
# Dragonpay

## Structure

`Dragonpay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `issuer` | `string` | Required | The Dragonpay issuer value of the shopper's selected bank. Set this to an **id** of a Dragonpay issuer to preselect it. | getIssuer(): string | setIssuer(string issuer): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperEmail` | `?string` | Optional | The shopper’s email address. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `type` | [`string(Type23)`](../../doc/models/type-23.md) | Required | **dragonpay** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId8",
  "issuer": "issuer2",
  "sdkData": "sdkData2",
  "shopperEmail": "shopperEmail6",
  "type": "dragonpay_otc_non_banking"
}
```

