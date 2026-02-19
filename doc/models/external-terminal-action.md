
# External Terminal Action

## Structure

`ExternalTerminalAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actionType` | `?string` | Optional | The type of terminal action: **InstallAndroidApp**, **UninstallAndroidApp**, **InstallAndroidCertificate**, or **UninstallAndroidCertificate**. | getActionType(): ?string | setActionType(?string actionType): void |
| `config` | `?string` | Optional | Technical information about the terminal action. | getConfig(): ?string | setConfig(?string config): void |
| `confirmedAt` | `?DateTime` | Optional | The date and time when the action was carried out. | getConfirmedAt(): ?\DateTime | setConfirmedAt(?\DateTime confirmedAt): void |
| `id` | `?string` | Optional | The unique ID of the terminal action. | getId(): ?string | setId(?string id): void |
| `result` | `?string` | Optional | The result message for the action. | getResult(): ?string | setResult(?string result): void |
| `scheduledAt` | `?DateTime` | Optional | The date and time when the action was scheduled to happen. | getScheduledAt(): ?\DateTime | setScheduledAt(?\DateTime scheduledAt): void |
| `status` | `?string` | Optional | The status of the terminal action: **pending**, **successful**, **failed**, **cancelled**, or **tryLater**. | getStatus(): ?string | setStatus(?string status): void |
| `terminalId` | `?string` | Optional | The unique ID of the terminal that the action applies to. | getTerminalId(): ?string | setTerminalId(?string terminalId): void |

## Example (as JSON)

```json
{
  "actionType": "actionType6",
  "config": "config2",
  "confirmedAt": "2016-03-13T12:52:32.123Z",
  "id": "id6",
  "result": "result0"
}
```

