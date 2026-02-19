
# Offline Processing

## Structure

`OfflineProcessing`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `chipFloorLimit` | `?int` | Optional | The maximum offline transaction amount for chip cards, in the processing currency and specified in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getChipFloorLimit(): ?int | setChipFloorLimit(?int chipFloorLimit): void |
| `offlineSwipeLimits` | [`?(MinorUnitsMonetaryValue[])`](../../doc/models/minor-units-monetary-value.md) | Optional | The maximum offline transaction amount for swiped cards, in the specified currency. | getOfflineSwipeLimits(): ?array | setOfflineSwipeLimits(?array offlineSwipeLimits): void |

## Example (as JSON)

```json
{
  "chipFloorLimit": 146,
  "offlineSwipeLimits": [
    {
      "amount": 136,
      "currencyCode": "currencyCode8"
    }
  ]
}
```

