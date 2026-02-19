
# Refunds

## Structure

`Refunds`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `referenced` | [`?Referenced1`](../../doc/models/referenced-1.md) | Optional | Settings for referenced refunds. | getReferenced(): ?Referenced1 | setReferenced(?Referenced1 referenced): void |
| `unreferenced` | [`?Unreferenced2`](../../doc/models/unreferenced-2.md) | Optional | Settings for unreferenced refunds. | getUnreferenced(): ?Unreferenced2 | setUnreferenced(?Unreferenced2 unreferenced): void |

## Example (as JSON)

```json
{
  "referenced": {
    "enableStandaloneRefunds": false
  },
  "unreferenced": {
    "enableUnreferencedRefunds": false
  }
}
```

