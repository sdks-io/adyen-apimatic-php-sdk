
# Invalid Field

*This model accepts additional fields of type array.*

## Structure

`InvalidField`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | The field that has an invalid value. | getName(): string | setName(string name): void |
| `value` | `string` | Required | The invalid value. | getValue(): string | setValue(string value): void |
| `message` | `string` | Required | Description of the validation error. | getMessage(): string | setMessage(string message): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "name": "name8",
  "value": "value0",
  "message": "message2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

