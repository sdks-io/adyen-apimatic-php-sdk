
# Response Additional Data Network Tokens

## Structure

`ResponseAdditionalDataNetworkTokens`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `networkTokenAvailable` | `?string` | Optional | Indicates whether a network token is available for the specified card. | getNetworkTokenAvailable(): ?string | setNetworkTokenAvailable(?string networkTokenAvailable): void |
| `networkTokenBin` | `?string` | Optional | The Bank Identification Number of a tokenized card, which is the first six digits of a card number. | getNetworkTokenBin(): ?string | setNetworkTokenBin(?string networkTokenBin): void |
| `networkTokenTokenSummary` | `?string` | Optional | The last four digits of a network token. | getNetworkTokenTokenSummary(): ?string | setNetworkTokenTokenSummary(?string networkTokenTokenSummary): void |

## Example (as JSON)

```json
{
  "networkToken.available": "networkToken.available8",
  "networkToken.bin": "networkToken.bin0",
  "networkToken.tokenSummary": "networkToken.tokenSummary4"
}
```

