
# Commission

## Structure

`Commission`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `fixedAmount` | `?int` | Optional | A fixed commission fee, in minor units. | getFixedAmount(): ?int | setFixedAmount(?int fixedAmount): void |
| `variablePercentage` | `?int` | Optional | A variable commission fee, in basis points. | getVariablePercentage(): ?int | setVariablePercentage(?int variablePercentage): void |

## Example (as JSON)

```json
{
  "fixedAmount": 204,
  "variablePercentage": 112
}
```

