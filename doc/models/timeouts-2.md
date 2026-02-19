
# Timeouts 2

Settings for device [time-outs](https://docs.adyen.com/point-of-sale/pos-timeouts#device-time-out).

## Structure

`Timeouts2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `fromActiveToSleep` | `?int` | Optional | Indicates the number of seconds of inactivity after which the terminal display goes into sleep mode. | getFromActiveToSleep(): ?int | setFromActiveToSleep(?int fromActiveToSleep): void |

## Example (as JSON)

```json
{
  "fromActiveToSleep": 78
}
```

