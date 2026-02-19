
# Terminal Connectivity

## Structure

`TerminalConnectivity`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bluetooth` | [`?TerminalConnectivityBluetooth`](../../doc/models/terminal-connectivity-bluetooth.md) | Optional | - | getBluetooth(): ?TerminalConnectivityBluetooth | setBluetooth(?TerminalConnectivityBluetooth bluetooth): void |
| `cellular` | [`?TerminalConnectivityCellular`](../../doc/models/terminal-connectivity-cellular.md) | Optional | - | getCellular(): ?TerminalConnectivityCellular | setCellular(?TerminalConnectivityCellular cellular): void |
| `ethernet` | [`?TerminalConnectivityEthernet`](../../doc/models/terminal-connectivity-ethernet.md) | Optional | - | getEthernet(): ?TerminalConnectivityEthernet | setEthernet(?TerminalConnectivityEthernet ethernet): void |
| `wifi` | [`?TerminalConnectivityWifi`](../../doc/models/terminal-connectivity-wifi.md) | Optional | - | getWifi(): ?TerminalConnectivityWifi | setWifi(?TerminalConnectivityWifi wifi): void |

## Example (as JSON)

```json
{
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
}
```

