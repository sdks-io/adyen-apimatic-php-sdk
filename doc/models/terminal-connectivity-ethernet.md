
# Terminal Connectivity Ethernet

## Structure

`TerminalConnectivityEthernet`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipAddress` | `?string` | Optional | The terminal's ethernet IP address. | getIpAddress(): ?string | setIpAddress(?string ipAddress): void |
| `linkNegotiation` | `?string` | Optional | The ethernet link negotiation that the terminal uses. | getLinkNegotiation(): ?string | setLinkNegotiation(?string linkNegotiation): void |
| `macAddress` | `?string` | Optional | The terminal's ethernet MAC address. | getMacAddress(): ?string | setMacAddress(?string macAddress): void |

## Example (as JSON)

```json
{
  "ipAddress": "ipAddress6",
  "linkNegotiation": "linkNegotiation0",
  "macAddress": "macAddress2"
}
```

