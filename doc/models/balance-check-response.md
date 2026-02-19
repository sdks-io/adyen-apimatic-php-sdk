
# Balance Check Response

## Structure

`BalanceCheckResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `additionalData` | `?array<string,string>` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first: Go to **Customer Area** > **Developers** > **Additional data**. | getAdditionalData(): ?array | setAdditionalData(?array additionalData): void |
| `balance` | [`Amount8`](../../doc/models/amount-8.md) | Required | The balance for the payment method. | getBalance(): Amount8 | setBalance(Amount8 balance): void |
| `fraudResult` | [`?FraudResult1`](../../doc/models/fraud-result-1.md) | Optional | The fraud result properties of the payment. | getFraudResult(): ?FraudResult1 | setFraudResult(?FraudResult1 fraudResult): void |
| `pspReference` | `?string` | Optional | Adyen's 16-character reference associated with the transaction/request. This value is globally unique; quote it when communicating with us about this request. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `refusalReason` | `?string` | Optional | If the payment's authorisation is refused or an error occurs during authorisation, this field holds Adyen's mapped reason for the refusal or a description of the error. When a transaction fails, the authorisation response includes `resultCode` and `refusalReason` values.<br><br>For more information, see [Refusal reasons](https://docs.adyen.com/development-resources/refusal-reasons). | getRefusalReason(): ?string | setRefusalReason(?string refusalReason): void |
| `resultCode` | [`string(ResultCode)`](../../doc/models/result-code.md) | Required | The result of the cancellation request.<br><br>Possible values:<br><br>* **Success** – Indicates that the balance check was successful.<br>* **NotEnoughBalance** – Commonly indicates that the card did not have enough balance to pay the amount in the request, or that the currency of the balance on the card did not match the currency of the requested amount.<br>* **Failed** – Indicates that the balance check failed. | getResultCode(): string | setResultCode(string resultCode): void |
| `transactionLimit` | [`?Amount9`](../../doc/models/amount-9.md) | Optional | The maximum spendable balance for a single transaction. Applicable to some gift cards. | getTransactionLimit(): ?Amount9 | setTransactionLimit(?Amount9 transactionLimit): void |

## Example (as JSON)

```json
{
  "additionalData": {
    "key0": "additionalData6"
  },
  "balance": {
    "currency": "currency4",
    "value": 128
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
  "pspReference": "pspReference8",
  "refusalReason": "refusalReason6",
  "resultCode": "Success",
  "transactionLimit": {
    "currency": "currency4",
    "value": 238
  }
}
```

