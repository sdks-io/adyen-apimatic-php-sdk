
# Install Android App Details

## Structure

`InstallAndroidAppDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appId` | `?string` | Optional | The unique identifier of the app to be installed. | getAppId(): ?string | setAppId(?string appId): void |
| `type` | [`?string(Type27)`](../../doc/models/type-27.md) | Optional | Type of terminal action: Install an Android app.<br><br>**Default**: `Type27::INSTALLANDROIDAPP` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "InstallAndroidApp",
  "appId": "appId6"
}
```

