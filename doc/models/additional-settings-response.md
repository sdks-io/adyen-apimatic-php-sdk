
# Additional Settings Response

## Structure

`AdditionalSettingsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `excludeEventCodes` | `?(string[])` | Optional | Object containing list of event codes for which the notification will not be sent. | getExcludeEventCodes(): ?array | setExcludeEventCodes(?array excludeEventCodes): void |
| `includeEventCodes` | `?(string[])` | Optional | Object containing list of event codes for which the notification will be sent. | getIncludeEventCodes(): ?array | setIncludeEventCodes(?array includeEventCodes): void |
| `properties` | `?array<string,bool>` | Optional | Object containing boolean key-value pairs. The key can be any [standard webhook additional setting](https://docs.adyen.com/development-resources/webhooks/additional-settings), and the value indicates if the setting is enabled.<br>For example, `includeCaptureDelayHours`: **true** means the standard notifications you get will contain the number of hours remaining until the payment will be captured. | getProperties(): ?array | setProperties(?array properties): void |

## Example (as JSON)

```json
{
  "excludeEventCodes": [
    "excludeEventCodes6",
    "excludeEventCodes7",
    "excludeEventCodes8"
  ],
  "includeEventCodes": [
    "includeEventCodes4",
    "includeEventCodes5",
    "includeEventCodes6"
  ],
  "properties": {
    "key0": false
  }
}
```

