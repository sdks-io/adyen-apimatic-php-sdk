
# Release Update Details

## Structure

`ReleaseUpdateDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`?string(Type53)`](../../doc/models/type-53.md) | Optional | Type of terminal action: Update Release.<br><br>**Default**: `Type53::RELEASEUPDATE` | getType(): ?string | setType(?string type): void |
| `updateAtFirstMaintenanceCall` | `?bool` | Optional | Boolean flag that tells if the terminal should update at the first next maintenance call. If false, terminal will update on its configured reboot time. | getUpdateAtFirstMaintenanceCall(): ?bool | setUpdateAtFirstMaintenanceCall(?bool updateAtFirstMaintenanceCall): void |

## Example (as JSON)

```json
{
  "type": "ReleaseUpdate",
  "updateAtFirstMaintenanceCall": false
}
```

