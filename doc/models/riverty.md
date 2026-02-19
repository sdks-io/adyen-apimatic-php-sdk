
# Riverty

*This model accepts additional fields of type array.*

## Structure

`Riverty`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingAddress` | `?string` | Optional | The address where to send the invoice. | getBillingAddress(): ?string | setBillingAddress(?string billingAddress): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `deliveryAddress` | `?string` | Optional | The address where the goods should be delivered. | getDeliveryAddress(): ?string | setDeliveryAddress(?string deliveryAddress): void |
| `deviceFingerprint` | `?string` | Optional | A string containing the shopper's device fingerprint. For more information, refer to [Device fingerprinting](https://docs.adyen.com/risk-management/device-fingerprinting).<br><br>**Constraints**: *Maximum Length*: `5000` | getDeviceFingerprint(): ?string | setDeviceFingerprint(?string deviceFingerprint): void |
| `iban` | `?string` | Optional | The iban number of the customer<br><br>**Constraints**: *Maximum Length*: `34` | getIban(): ?string | setIban(?string iban): void |
| `personalDetails` | `?string` | Optional | Shopper name, date of birth, phone number, and email address. | getPersonalDetails(): ?string | setPersonalDetails(?string personalDetails): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `subtype` | `?string` | Optional | The payment method subtype. | getSubtype(): ?string | setSubtype(?string subtype): void |
| `type` | [`string(Type43)`](../../doc/models/type-43.md) | Required | **riverty**<br><br>**Default**: `Type43::RIVERTY` | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "riverty",
  "billingAddress": "billingAddress2",
  "checkoutAttemptId": "checkoutAttemptId0",
  "deliveryAddress": "deliveryAddress0",
  "deviceFingerprint": "deviceFingerprint0",
  "iban": "iban8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

