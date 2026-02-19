
# Voucher

## Structure

`Voucher`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `firstName` | `string` | Required | The shopper's first name. | getFirstName(): string | setFirstName(string firstName): void |
| `lastName` | `string` | Required | The shopper's last name. | getLastName(): string | setLastName(string lastName): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `shopperEmail` | `string` | Required | The shopper's email. | getShopperEmail(): string | setShopperEmail(string shopperEmail): void |
| `telephoneNumber` | `string` | Required | The shopper's contact number. It must have an international number format, for example **+31 20 779 1846**. Formats like **+31 (0)20 779 1846** or **0031 20 779 1846** are not accepted. | getTelephoneNumber(): string | setTelephoneNumber(string telephoneNumber): void |
| `type` | [`string(Type24)`](../../doc/models/type-24.md) | Required | **econtextvoucher** | getType(): string | setType(string type): void |

## Example (as JSON)

```json
{
  "checkoutAttemptId": "checkoutAttemptId4",
  "firstName": "firstName6",
  "lastName": "lastName2",
  "sdkData": "sdkData2",
  "shopperEmail": "shopperEmail2",
  "telephoneNumber": "telephoneNumber0",
  "type": "econtext_stores"
}
```

