
# Checkout Forward Request Options 2

The customizations that can be applied when making a forward request.

## Structure

`CheckoutForwardRequestOptions2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountUpdate` | `?bool` | Optional | Whether to check for a card account update (true) or not (false) | getAccountUpdate(): ?bool | setAccountUpdate(?bool accountUpdate): void |
| `dryRun` | `?bool` | Optional | Set to **true** to receive a copy of the request Adyen is making to the third party in the response. Any sensitive information will be masked in the response you receive. This functionality is only available in the test environment. | getDryRun(): ?bool | setDryRun(?bool dryRun): void |
| `networkToken` | [`?CheckoutNetworkTokenOption2`](../../doc/models/checkout-network-token-option-2.md) | Optional | The object that contains the details for forwarding a network token. | getNetworkToken(): ?CheckoutNetworkTokenOption2 | setNetworkToken(?CheckoutNetworkTokenOption2 networkToken): void |
| `networkTxReferencePaths` | `?(string[])` | Optional | Set in tokenize:true case when forwarding PAN. Addresses to the possible location(s) of networkTxReference in the incoming 3rd party response | getNetworkTxReferencePaths(): ?array | setNetworkTxReferencePaths(?array networkTxReferencePaths): void |
| `tokenize` | `?bool` | Optional | Set to **true**, the payment details are [tokenized](https://docs.adyen.com/online-payments/tokenization). | getTokenize(): ?bool | setTokenize(?bool tokenize): void |

## Example (as JSON)

```json
{
  "accountUpdate": false,
  "dryRun": false,
  "networkToken": {
    "includeCryptogram": false,
    "useNetworkToken": false
  },
  "networkTxReferencePaths": [
    "networkTxReferencePaths3",
    "networkTxReferencePaths4"
  ],
  "tokenize": false
}
```

