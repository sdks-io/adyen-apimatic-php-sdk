
# Hardware

## Structure

`Hardware`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `displayMaximumBackLight` | `?int` | Optional | The brightness of the display when the terminal is being used, expressed as a percentage. | getDisplayMaximumBackLight(): ?int | setDisplayMaximumBackLight(?int displayMaximumBackLight): void |
| `resetTotalsHour` | `?int` | Optional | The hour of the day when the terminal is set to reset the Totals report. By default, the reset hour is at 6:00 AM in the timezone of the terminal. Minimum value: 0, maximum value: 23. | getResetTotalsHour(): ?int | setResetTotalsHour(?int resetTotalsHour): void |
| `restartHour` | `?int` | Optional | The hour of the day when the terminal is set to reboot to apply the configuration and software updates. By default, the restart hour is at 6:00 AM in the timezone of the terminal. Minimum value: 0, maximum value: 23. | getRestartHour(): ?int | setRestartHour(?int restartHour): void |

## Example (as JSON)

```json
{
  "displayMaximumBackLight": 158,
  "resetTotalsHour": 148,
  "restartHour": 126
}
```

