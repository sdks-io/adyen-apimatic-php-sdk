
# Valuelink Info

## Structure

`ValuelinkInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authorisationMid` | `string` | Required | Authorisation Mid | getAuthorisationMid(): string | setAuthorisationMid(string authorisationMid): void |
| `pinSupport` | [`string(PinSupport)`](../../doc/models/pin-support.md) | Required | PIN Support. For ecommerce, PIN is required. | getPinSupport(): string | setPinSupport(string pinSupport): void |
| `submitterId` | `?string` | Optional | Submitter ID | getSubmitterId(): ?string | setSubmitterId(?string submitterId): void |
| `terminalId` | `?string` | Optional | Terminal ID | getTerminalId(): ?string | setTerminalId(?string terminalId): void |

## Example (as JSON)

```json
{
  "authorisationMid": "authorisationMid2",
  "pinSupport": "PIN",
  "submitterId": "submitterId8",
  "terminalId": "terminalId4"
}
```

