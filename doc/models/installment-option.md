
# Installment Option

## Structure

`InstallmentOption`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `maxValue` | `?int` | Optional | The maximum number of installments offered for this payment method. | getMaxValue(): ?int | setMaxValue(?int maxValue): void |
| `plans` | [`?(string(Plan1)[])`](../../doc/models/plan-1.md) | Optional | Defines the type of installment plan. If not set, defaults to **regular**.<br><br>Possible values:<br><br>* **regular**<br>* **revolving** | getPlans(): ?array | setPlans(?array plans): void |
| `preselectedValue` | `?int` | Optional | Preselected number of installments offered for this payment method. | getPreselectedValue(): ?int | setPreselectedValue(?int preselectedValue): void |
| `values` | `?(int[])` | Optional | An array of the number of installments that the shopper can choose from. For example, **[2,3,5]**. This cannot be specified simultaneously with `maxValue`. | getValues(): ?array | setValues(?array values): void |

## Example (as JSON)

```json
{
  "maxValue": 0,
  "plans": [
    "nointerest_bonus",
    "refund_prctg",
    "regular"
  ],
  "preselectedValue": 100,
  "values": [
    222
  ]
}
```

