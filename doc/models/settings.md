
# Settings

## Structure

`Settings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `band` | `?string` | Optional | The preferred Wi-Fi band, for use if the terminals support multiple bands. Possible values: All, 2.4GHz, 5GHz. | getBand(): ?string | setBand(?string band): void |
| `roaming` | `?bool` | Optional | Indicates whether roaming is enabled on the terminals. | getRoaming(): ?bool | setRoaming(?bool roaming): void |
| `timeout` | `?int` | Optional | The connection time-out in seconds. Minimum value: 0. | getTimeout(): ?int | setTimeout(?int timeout): void |

## Example (as JSON)

```json
{
  "band": "band2",
  "roaming": false,
  "timeout": 56
}
```

