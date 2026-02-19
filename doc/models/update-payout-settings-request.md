
# Update Payout Settings Request

## Structure

`UpdatePayoutSettingsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `?bool` | Optional | Indicates if payouts to this bank account are enabled. Default: **true**.<br><br>To receive payouts into this bank account, both `enabled` and `allowed` must be **true**. | getEnabled(): ?bool | setEnabled(?bool enabled): void |

## Example (as JSON)

```json
{
  "enabled": false
}
```

