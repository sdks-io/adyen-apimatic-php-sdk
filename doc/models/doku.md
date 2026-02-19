
# Doku

## Structure

`Doku`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `firstName` | `string` | Required | The shopper's first name. | getFirstName(): string | setFirstName(string firstName): void |
| `lastName` | `string` | Required | The shopper's last name. | getLastName(): string | setLastName(string lastName): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperEmail` | `string` | Required | The shopper's email. | getShopperEmail(): string | setShopperEmail(string shopperEmail): void |
| `type` | [`string(Type19)`](../../doc/models/type-19.md) | Required | **doku** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId4",
  "firstName": "firstName6",
  "lastName": "lastName2",
  "sdkData": "sdkData2",
  "shopperEmail": "shopperEmail8",
  "type": "doku_bni_va"
}
```

