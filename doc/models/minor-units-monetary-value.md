
# Minor Units Monetary Value

## Structure

`MinorUnitsMonetaryValue`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?int` | Optional | The transaction amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getAmount(): ?int | setAmount(?int amount): void |
| `currencyCode` | `?string` | Optional | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |

## Example (as JSON)

```json
{
  "amount": 196,
  "currencyCode": "currencyCode0"
}
```

