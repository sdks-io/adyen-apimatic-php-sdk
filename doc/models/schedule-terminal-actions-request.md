
# Schedule Terminal Actions Request

## Structure

`ScheduleTerminalActionsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actionDetails` | [ForceRebootDetails](../../doc/models/force-reboot-details.md)\|[InstallAndroidAppDetails](../../doc/models/install-android-app-details.md)\|[InstallAndroidCertificateDetails](../../doc/models/install-android-certificate-details.md)\|[ReleaseUpdateDetails](../../doc/models/release-update-details.md)\|[UninstallAndroidAppDetails](../../doc/models/uninstall-android-app-details.md)\|[UninstallAndroidCertificateDetails](../../doc/models/uninstall-android-certificate-details.md)\|null | Optional | This is a container for one-of cases. | getActionDetails(): | setActionDetails( actionDetails): void |
| `scheduledAt` | `?string` | Optional | The date and time when the action should happen.<br>Format: [RFC 3339](https://www.rfc-editor.org/rfc/rfc3339), but without the **Z** before the time offset. For example, **2021-11-15T12:16:21+0100**<br>The action is sent with the first [maintenance call](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api#when-actions-take-effect) after the specified date and time in the time zone of the terminal.<br>An empty value causes the action to be sent as soon as possible: at the next maintenance call. | getScheduledAt(): ?string | setScheduledAt(?string scheduledAt): void |
| `storeId` | `?string` | Optional | The unique ID of the [store](https://docs.adyen.com/api-explorer/#/ManagementService/latest/get/stores). If present, all terminals in the `terminalIds` list must be assigned to this store. | getStoreId(): ?string | setStoreId(?string storeId): void |
| `terminalIds` | `?(string[])` | Optional | A list of unique IDs of the terminals to apply the action to. You can extract the IDs from the [GET `/terminals`](https://docs.adyen.com/api-explorer/#/ManagementService/latest/get/terminals) response. Maximum length: 100 IDs. | getTerminalIds(): ?array | setTerminalIds(?array terminalIds): void |

## Example (as JSON)

```json
{
  "actionDetails": {
    "type": "ForceReboot"
  },
  "scheduledAt": "scheduledAt6",
  "storeId": "storeId4",
  "terminalIds": [
    "terminalIds2",
    "terminalIds3"
  ]
}
```

