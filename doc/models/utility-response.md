
# Utility Response

## Structure

`UtilityResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `originKeys` | `?array<string,string>` | Optional | The list of origin keys for all requested domains. For each list item, the key is the domain and the value is the origin key. | getOriginKeys(): ?array | setOriginKeys(?array originKeys): void |

## Example (as JSON)

```json
{
  "originKeys": {
    "key0": "originKeys6",
    "key1": "originKeys7"
  }
}
```

