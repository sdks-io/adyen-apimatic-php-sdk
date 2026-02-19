
# Create Order Response

## Structure

`CreateOrderResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `additionalData` | `?array<string,string>` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first: Go to **Customer Area** > **Developers** > **Additional data**. | getAdditionalData(): ?array | setAdditionalData(?array additionalData): void |
| `amount` | [`Amount11`](../../doc/models/amount-11.md) | Required | The initial amount of the order. | getAmount(): Amount11 | setAmount(Amount11 amount): void |
| `expiresAt` | `string` | Required | The date that the order will expire. | getExpiresAt(): string | setExpiresAt(string expiresAt): void |
| `fraudResult` | [`?FraudResult1`](../../doc/models/fraud-result-1.md) | Optional | The fraud result properties of the payment. | getFraudResult(): ?FraudResult1 | setFraudResult(?FraudResult1 fraudResult): void |
| `orderData` | `string` | Required | The encrypted data that will be used by merchant for adding payments to the order. | getOrderData(): string | setOrderData(string orderData): void |
| `pspReference` | `?string` | Optional | Adyen's 16-character reference associated with the transaction/request. This value is globally unique; quote it when communicating with us about this request. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `reference` | `?string` | Optional | The reference provided by merchant for creating the order. | getReference(): ?string | setReference(?string reference): void |
| `refusalReason` | `?string` | Optional | If the payment's authorisation is refused or an error occurs during authorisation, this field holds Adyen's mapped reason for the refusal or a description of the error. When a transaction fails, the authorisation response includes `resultCode` and `refusalReason` values.<br><br>For more information, see [Refusal reasons](https://docs.adyen.com/development-resources/refusal-reasons). | getRefusalReason(): ?string | setRefusalReason(?string refusalReason): void |
| `remainingAmount` | [`Amount22`](../../doc/models/amount-22.md) | Required | The remaining amount in the order. | getRemainingAmount(): Amount22 | setRemainingAmount(Amount22 remainingAmount): void |
| `resultCode` | `string` | Required, Constant | The result of the order creation request.<br>The value is always **Success**.<br><br>**Value**: `'Success'` | getResultCode(): string | setResultCode(string resultCode): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt4",
  "orderData": "orderData0",
  "remainingAmount": {
    "currency": "currency6",
    "value": 156
  },
  "resultCode": "Success",
  "additionalData": {
    "key0": "additionalData8",
    "key1": "additionalData9"
  },
  "fraudResult": {
    "accountScore": 232,
    "results": [
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      },
      {
        "accountScore": 102,
        "checkId": 246,
        "name": "name6"
      }
    ]
  },
  "pspReference": "pspReference0",
  "reference": "reference6",
  "refusalReason": "refusalReason8"
}
```

