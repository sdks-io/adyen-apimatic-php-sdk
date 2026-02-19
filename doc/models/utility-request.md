
# Utility Request

## Structure

`UtilityRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `originDomains` | `string[]` | Required | The list of origin domains, for which origin keys are requested. | getOriginDomains(): array | setOriginDomains(array originDomains): void |

## Example (as JSON)

```json
{
  "originDomains": [
    "originDomains2",
    "originDomains3",
    "originDomains4"
  ]
}
```

