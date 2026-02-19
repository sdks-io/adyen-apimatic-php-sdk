
# Create Order Request

## Structure

`CreateOrderRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`Amount20`](../../doc/models/amount-20.md) | Required | The total amount of the order. | getAmount(): Amount20 | setAmount(Amount20 amount): void |
| `expiresAt` | `?string` | Optional | The date when the order should expire. If not provided, the default expiry duration is 1 day.<br><br>[ISO 8601](https://www.w3.org/TR/NOTE-datetime) format: YYYY-MM-DDThh:mm:ss+TZD, for example, **2020-12-18T10:15:30+01:00**. | getExpiresAt(): ?string | setExpiresAt(?string expiresAt): void |
| `merchantAccount` | `string` | Required | The merchant account identifier, with which you want to process the order. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `reference` | `string` | Required | A custom reference identifying the order. | getReference(): string | setReference(string reference): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "expiresAt": "expiresAt4",
  "merchantAccount": "merchantAccount0",
  "reference": "reference4"
}
```

