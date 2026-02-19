
# Amounts

## Structure

`Amounts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes/). | getCurrency(): string | setCurrency(string currency): void |
| `values` | `int[]` | Required | The amounts of the donation (in [minor units](https://docs.adyen.com/development-resources/currency-codes/)). | getValues(): array | setValues(array values): void |

## Example (as JSON)

```json
{
  "currency": "currency0",
  "values": [
    214,
    213
  ]
}
```

