
# Schedule Terminal Actions Response

## Structure

`ScheduleTerminalActionsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actionDetails` | [ForceRebootDetails](../../doc/models/force-reboot-details.md)\|[InstallAndroidAppDetails](../../doc/models/install-android-app-details.md)\|[InstallAndroidCertificateDetails](../../doc/models/install-android-certificate-details.md)\|[ReleaseUpdateDetails](../../doc/models/release-update-details.md)\|[UninstallAndroidAppDetails](../../doc/models/uninstall-android-app-details.md)\|[UninstallAndroidCertificateDetails](../../doc/models/uninstall-android-certificate-details.md)\|null | Optional | This is a container for one-of cases. | getActionDetails(): | setActionDetails( actionDetails): void |
| `items` | [`?(TerminalActionScheduleDetail[])`](../../doc/models/terminal-action-schedule-detail.md) | Optional | A list containing a terminal ID and an action ID for each terminal that the action was scheduled for. | getItems(): ?array | setItems(?array items): void |
| `scheduledAt` | `?string` | Optional | The date and time when the action should happen.<br>Format: [RFC 3339](https://www.rfc-editor.org/rfc/rfc3339), but without the **Z** before the time offset. For example, **2021-11-15T12:16:21+0100**<br>The action is sent with the first [maintenance call](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api#when-actions-take-effect) after the specified date and time in the time zone of the terminal.<br>An empty value causes the action to be sent as soon as possible: at the next maintenance call. | getScheduledAt(): ?string | setScheduledAt(?string scheduledAt): void |
| `storeId` | `?string` | Optional | The unique ID of the [store](https://docs.adyen.com/api-explorer/#/ManagementService/latest/get/stores). If present, all terminals in the `terminalIds` list must be assigned to this store. | getStoreId(): ?string | setStoreId(?string storeId): void |
| `terminalsWithErrors` | `?array` | Optional | The validation errors that occurred in the list of terminals, and for each error the IDs of the terminals that the error applies to. | getTerminalsWithErrors(): ?array | setTerminalsWithErrors(?array terminalsWithErrors): void |
| `totalErrors` | `?int` | Optional | The number of terminals for which scheduling the action failed. | getTotalErrors(): ?int | setTotalErrors(?int totalErrors): void |
| `totalScheduled` | `?int` | Optional | The number of terminals for which the action was successfully scheduled. This doesn't mean the action has happened yet. | getTotalScheduled(): ?int | setTotalScheduled(?int totalScheduled): void |

## Example (as JSON)

```json
{
  "actionDetails": {
    "type": "ForceReboot"
  },
  "items": [
    {
      "id": "id8",
      "terminalId": "terminalId6"
    },
    {
      "id": "id8",
      "terminalId": "terminalId6"
    },
    {
      "id": "id8",
      "terminalId": "terminalId6"
    }
  ],
  "scheduledAt": "scheduledAt8",
  "storeId": "storeId4",
  "terminalsWithErrors": {
    "key0": {
      "key1": "val1",
      "key2": "val2"
    },
    "key1": {
      "key1": "val1",
      "key2": "val2"
    },
    "key2": {
      "key1": "val1",
      "key2": "val2"
    }
  }
}
```

