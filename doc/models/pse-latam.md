
# Pse Latam

*This model accepts additional fields of type array.*

## Structure

`PseLatam`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bank` | `string` | Required | The shopper's bank. | getBank(): string | setBank(string bank): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `clientType` | `string` | Required | The client type. | getClientType(): string | setClientType(string clientType): void |
| `identification` | `string` | Required | The identification code. | getIdentification(): string | setIdentification(string identification): void |
| `identificationType` | `string` | Required | The identification type. | getIdentificationType(): string | setIdentificationType(string identificationType): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `type` | [`?string(Type40)`](../../doc/models/type-40.md) | Optional | The payment method type. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "bank": "bank4",
  "checkoutAttemptId": "checkoutAttemptId2",
  "clientType": "clientType4",
  "identification": "identification4",
  "identificationType": "identificationType8",
  "sdkData": "sdkData4",
  "type": "pse_payulatam",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

