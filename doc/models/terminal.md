
# Terminal

## Structure

`Terminal`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `assignment` | [`?TerminalAssignment2`](../../doc/models/terminal-assignment-2.md) | Optional | Indicates the account level to which the terminal is assigned, the [assignment status](https://docs.adyen.com/point-of-sale/automating-terminal-management/assign-terminals-api), and where the terminals is in the process of being reassigned to. | getAssignment(): ?TerminalAssignment2 | setAssignment(?TerminalAssignment2 assignment): void |
| `connectivity` | [`?TerminalConnectivity2`](../../doc/models/terminal-connectivity-2.md) | Optional | Information about bluetooth, cellular, ethernet and wifi connectivity for the terminal. | getConnectivity(): ?TerminalConnectivity2 | setConnectivity(?TerminalConnectivity2 connectivity): void |
| `firmwareVersion` | `?string` | Optional | The software release currently in use on the terminal. | getFirmwareVersion(): ?string | setFirmwareVersion(?string firmwareVersion): void |
| `id` | `?string` | Optional | The unique identifier of the terminal. | getId(): ?string | setId(?string id): void |
| `installedApKs` | [`?(InstalledApKs[])`](../../doc/models/installed-ap-ks.md) | Optional | A list of Android apps installed on the terminal. | getInstalledApKs(): ?array | setInstalledApKs(?array installedApKs): void |
| `lastActivityAt` | `?DateTime` | Optional | Date and time of the last activity on the terminal. Not included when the last activity was more than 14 days ago. | getLastActivityAt(): ?\DateTime | setLastActivityAt(?\DateTime lastActivityAt): void |
| `lastTransactionAt` | `?DateTime` | Optional | Date and time of the last transaction on the terminal. Not included when the last transaction was more than 14 days ago. | getLastTransactionAt(): ?\DateTime | setLastTransactionAt(?\DateTime lastTransactionAt): void |
| `model` | `?string` | Optional | The model name of the terminal. | getModel(): ?string | setModel(?string model): void |
| `restartLocalTime` | `?string` | Optional | The exact time of the terminal reboot, in the timezone of the terminal in **HH:mm** format. | getRestartLocalTime(): ?string | setRestartLocalTime(?string restartLocalTime): void |
| `serialNumber` | `?string` | Optional | The serial number of the terminal. | getSerialNumber(): ?string | setSerialNumber(?string serialNumber): void |

## Example (as JSON)

```json
{
  "assignment": {
    "companyId": "companyId6",
    "merchantId": "merchantId2",
    "reassignmentTarget": {
      "companyId": "companyId4",
      "inventory": false,
      "merchantId": "merchantId0",
      "storeId": "storeId8"
    },
    "status": "inventory",
    "storeId": "storeId0"
  },
  "connectivity": {
    "bluetooth": {
      "ipAddress": "ipAddress2",
      "macAddress": "macAddress2"
    },
    "cellular": {
      "iccid": "iccid6",
      "iccid2": "iccid24",
      "status": "deprecated"
    },
    "ethernet": {
      "ipAddress": "ipAddress2",
      "linkNegotiation": "linkNegotiation6",
      "macAddress": "macAddress2"
    },
    "wifi": {
      "ipAddress": "ipAddress8",
      "macAddress": "macAddress6",
      "ssid": "ssid4"
    }
  },
  "firmwareVersion": "firmwareVersion8",
  "id": "id6",
  "installedAPKs": [
    {
      "confirmationDate": "2016-03-13T12:52:32.123Z",
      "packageName": "packageName6",
      "versionName": "versionName6"
    }
  ]
}
```

