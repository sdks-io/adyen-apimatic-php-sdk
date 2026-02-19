
# Split Amount

## Structure

`SplitAmount`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `?string` | Optional | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). By default, this is the original payment currency.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` | getCurrency(): ?string | setCurrency(?string currency): void |
| `value` | `int` | Required | The value of the split amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getValue(): int | setValue(int value): void |

## Example (as JSON)

```json
{
  "currency": "currency8",
  "value": 54
}
```

