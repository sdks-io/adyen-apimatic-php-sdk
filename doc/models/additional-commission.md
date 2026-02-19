
# Additional Commission

## Structure

`AdditionalCommission`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `balanceAccountId` | `?string` | Optional | Unique identifier of the balance account to which the additional commission is booked. | getBalanceAccountId(): ?string | setBalanceAccountId(?string balanceAccountId): void |
| `fixedAmount` | `?int` | Optional | A fixed commission fee, in minor units. | getFixedAmount(): ?int | setFixedAmount(?int fixedAmount): void |
| `variablePercentage` | `?int` | Optional | A variable commission fee, in basis points. | getVariablePercentage(): ?int | setVariablePercentage(?int variablePercentage): void |

## Example (as JSON)

```json
{
  "balanceAccountId": "balanceAccountId8",
  "fixedAmount": 254,
  "variablePercentage": 166
}
```

