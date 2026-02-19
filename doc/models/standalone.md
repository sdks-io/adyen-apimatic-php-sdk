
# Standalone

## Structure

`Standalone`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currencyCode` | `?string` | Optional | The default currency of the standalone payment terminal as an [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) currency code.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `enableGratuities` | `?bool` | Optional | Indicates whether the tipping options specified in `gratuities` are enabled on the standalone terminal. | getEnableGratuities(): ?bool | setEnableGratuities(?bool enableGratuities): void |
| `enableStandalone` | `?bool` | Optional | Enable standalone mode. | getEnableStandalone(): ?bool | setEnableStandalone(?bool enableStandalone): void |

## Example (as JSON)

```json
{
  "currencyCode": "currencyCode2",
  "enableGratuities": false,
  "enableStandalone": false
}
```

