
# Supported Card Types 2

The type of card for which the terminal accepts store-and-forward payments. You can specify multiple card types.

## Structure

`SupportedCardTypes2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `credit` | `?bool` | Optional | Set to **true** to accept credit cards. | getCredit(): ?bool | setCredit(?bool credit): void |
| `debit` | `?bool` | Optional | Set to **true** to accept debit cards. | getDebit(): ?bool | setDebit(?bool debit): void |
| `deferredDebit` | `?bool` | Optional | Set to **true** to accept cards that allow deferred debit. | getDeferredDebit(): ?bool | setDeferredDebit(?bool deferredDebit): void |
| `prepaid` | `?bool` | Optional | Set to **true** to accept prepaid cards. | getPrepaid(): ?bool | setPrepaid(?bool prepaid): void |
| `unknown` | `?bool` | Optional | Set to **true** to accept card types for which the terminal can't determine the funding source while offline. | getUnknown(): ?bool | setUnknown(?bool unknown): void |

## Example (as JSON)

```json
{
  "credit": false,
  "debit": false,
  "deferredDebit": false,
  "prepaid": false,
  "unknown": false
}
```

