
# Split Configuration

## Structure

`SplitConfiguration`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `string` | Required | Your description for the split configuration.<br><br>**Constraints**: *Maximum Length*: `300` | getDescription(): string | setDescription(string description): void |
| `rules` | [`SplitConfigurationRule[]`](../../doc/models/split-configuration-rule.md) | Required | Array of rules that define the split configuration behavior. | getRules(): array | setRules(array rules): void |
| `splitConfigurationId` | `?string` | Optional | Unique identifier of the split configuration. | getSplitConfigurationId(): ?string | setSplitConfigurationId(?string splitConfigurationId): void |

## Example (as JSON)

```json
{
  "description": "description0",
  "rules": [
    {
      "cardRegion": "intraRegional",
      "currency": "currency2",
      "fundingSource": "prepaid",
      "paymentMethod": "paymentMethod4",
      "ruleId": "ruleId2",
      "shopperInteraction": "ANY",
      "splitLogic": {
        "acquiringFees": "deductFromLiableAccount",
        "additionalCommission": {
          "balanceAccountId": "balanceAccountId0",
          "fixedAmount": 100,
          "variablePercentage": 64
        },
        "adyenCommission": "deductFromLiableAccount",
        "adyenFees": "deductFromLiableAccount",
        "adyenMarkup": "deductFromLiableAccount",
        "commission": {
          "fixedAmount": 112,
          "variablePercentage": 52
        }
      }
    }
  ],
  "splitConfigurationId": "splitConfigurationId6"
}
```

