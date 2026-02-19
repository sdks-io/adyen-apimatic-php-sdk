
# Sub Input Detail

## Structure

`SubInputDetail`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `configuration` | `?array<string,string>` | Optional | Configuration parameters for the required input. | getConfiguration(): ?array | setConfiguration(?array configuration): void |
| `items` | [`?(Item[])`](../../doc/models/item.md) | Optional | In case of a select, the items to choose from. | getItems(): ?array | setItems(?array items): void |
| `key` | `?string` | Optional | The value to provide in the result. | getKey(): ?string | setKey(?string key): void |
| `optional` | `?bool` | Optional | True if this input is optional to provide. | getOptional(): ?bool | setOptional(?bool optional): void |
| `type` | `?string` | Optional | The type of the required input. | getType(): ?string | setType(?string type): void |
| `value` | `?string` | Optional | The value can be pre-filled, if available. | getValue(): ?string | setValue(?string value): void |

## Example (as JSON)

```json
{
  "configuration": {
    "key0": "configuration0",
    "key1": "configuration9"
  },
  "items": [
    {
      "id": "id8",
      "name": "name8"
    }
  ],
  "key": "key4",
  "optional": false,
  "type": "type6"
}
```

