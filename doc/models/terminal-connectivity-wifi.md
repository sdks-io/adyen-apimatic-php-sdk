
# Terminal Connectivity Wifi

## Structure

`TerminalConnectivityWifi`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipAddress` | `?string` | Optional | The terminal's IP address in the Wi-Fi network. | getIpAddress(): ?string | setIpAddress(?string ipAddress): void |
| `macAddress` | `?string` | Optional | The terminal's MAC address in the Wi-Fi network. | getMacAddress(): ?string | setMacAddress(?string macAddress): void |
| `ssid` | `?string` | Optional | The SSID of the Wi-Fi network that the terminal is connected to. | getSsid(): ?string | setSsid(?string ssid): void |

## Example (as JSON)

```json
{
  "ipAddress": "ipAddress2",
  "macAddress": "macAddress2",
  "ssid": "ssid0"
}
```

