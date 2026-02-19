
# Input Detail

## Structure

`InputDetail`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `configuration` | `?array<string,string>` | Optional | Configuration parameters for the required input. | getConfiguration(): ?array | setConfiguration(?array configuration): void |
| `details` | [`?(SubInputDetail[])`](../../doc/models/sub-input-detail.md) | Optional | Input details can also be provided recursively. | getDetails(): ?array | setDetails(?array details): void |
| `inputDetails` | [`?(SubInputDetail[])`](../../doc/models/sub-input-detail.md) | Optional | Input details can also be provided recursively (deprecated). | getInputDetails(): ?array | setInputDetails(?array inputDetails): void |
| `itemSearchUrl` | `?string` | Optional | In case of a select, the URL from which to query the items. | getItemSearchUrl(): ?string | setItemSearchUrl(?string itemSearchUrl): void |
| `items` | [`?(Item[])`](../../doc/models/item.md) | Optional | In case of a select, the items to choose from. | getItems(): ?array | setItems(?array items): void |
| `key` | `?string` | Optional | The value to provide in the result. | getKey(): ?string | setKey(?string key): void |
| `optional` | `?bool` | Optional | True if this input value is optional. | getOptional(): ?bool | setOptional(?bool optional): void |
| `type` | `?string` | Optional | The type of the required input. | getType(): ?string | setType(?string type): void |
| `value` | `?string` | Optional | The value can be pre-filled, if available. | getValue(): ?string | setValue(?string value): void |

## Example (as JSON)

```json
{
  "configuration": {
    "key0": "configuration0",
    "key1": "configuration1",
    "key2": "configuration2"
  },
  "details": [
    {
      "configuration": {
        "key0": "configuration6",
        "key1": "configuration7"
      },
      "items": [
        {
          "id": "id8",
          "name": "name8"
        }
      ],
      "key": "key0",
      "optional": false,
      "type": "type0"
    },
    {
      "configuration": {
        "key0": "configuration6",
        "key1": "configuration7"
      },
      "items": [
        {
          "id": "id8",
          "name": "name8"
        }
      ],
      "key": "key0",
      "optional": false,
      "type": "type0"
    },
    {
      "configuration": {
        "key0": "configuration6",
        "key1": "configuration7"
      },
      "items": [
        {
          "id": "id8",
          "name": "name8"
        }
      ],
      "key": "key0",
      "optional": false,
      "type": "type0"
    }
  ],
  "inputDetails": [
    {
      "configuration": {
        "key0": "configuration6"
      },
      "items": [
        {
          "id": "id8",
          "name": "name8"
        },
        {
          "id": "id8",
          "name": "name8"
        },
        {
          "id": "id8",
          "name": "name8"
        }
      ],
      "key": "key0",
      "optional": false,
      "type": "type0"
    },
    {
      "configuration": {
        "key0": "configuration6"
      },
      "items": [
        {
          "id": "id8",
          "name": "name8"
        },
        {
          "id": "id8",
          "name": "name8"
        },
        {
          "id": "id8",
          "name": "name8"
        }
      ],
      "key": "key0",
      "optional": false,
      "type": "type0"
    }
  ],
  "itemSearchUrl": "itemSearchUrl0",
  "items": [
    {
      "id": "id8",
      "name": "name8"
    },
    {
      "id": "id8",
      "name": "name8"
    }
  ]
}
```

