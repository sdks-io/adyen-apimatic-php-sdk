
# Uninstall Android App Details

*This model accepts additional fields of type array.*

## Structure

`UninstallAndroidAppDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appId` | `?string` | Optional | The unique identifier of the app to be uninstalled. | getAppId(): ?string | setAppId(?string appId): void |
| `type` | [`?string(Type61)`](../../doc/models/type-61.md) | Optional | Type of terminal action: Uninstall an Android app.<br><br>**Default**: `Type61::UNINSTALLANDROIDAPP` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "UninstallAndroidApp",
  "appId": "appId0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

