
# Upi Payment Method

*This model accepts additional fields of type array.*

## Structure

`UpiPaymentMethod`

## Inherits From

[`ShopperIdPaymentMethod`](../../doc/models/shopper-id-payment-method.md)

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `virtualPaymentAddress` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getVirtualPaymentAddress(): ?string | setVirtualPaymentAddress(?string virtualPaymentAddress): void |
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

