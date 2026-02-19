
# Shopper Id Payment Method

*This model accepts additional fields of type array.*

## Structure

`ShopperIdPaymentMethod`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | `?string` | Optional | - | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "upi_collect",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  },
  "virtualPaymentAddress": "virtualPaymentAddress4"
}
```

