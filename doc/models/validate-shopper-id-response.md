
# Validate Shopper Id Response

*This model accepts additional fields of type array.*

## Structure

`ValidateShopperIdResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reason` | `?string` | Optional | Reason for the result. | getReason(): ?string | setReason(?string reason): void |
| `result` | [`?string(Result1)`](../../doc/models/result-1.md) | Optional | Result of the validation. Ex: valid, invalid, unknown | getResult(): ?string | setResult(?string result): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "reason": "reason8",
  "result": "INVALID",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

