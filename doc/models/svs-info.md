
# Svs Info

## Structure

`SvsInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authorisationMid` | `string` | Required | The merchant ID (MID) that the acquirer recognizes you by. | getAuthorisationMid(): string | setAuthorisationMid(string authorisationMid): void |
| `currencyCode` | `string` | Required | The three-character ISO currency code, example **USD** | getCurrencyCode(): string | setCurrencyCode(string currencyCode): void |

## Example (as JSON)

```json
{
  "authorisationMid": "authorisationMid2",
  "currencyCode": "currencyCode6"
}
```

