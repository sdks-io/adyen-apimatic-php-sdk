
# Checkout Network Token Option 2

The object that contains the details for forwarding a network token.

## Structure

`CheckoutNetworkTokenOption2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `includeCryptogram` | `?bool` | Optional | Set to **true** to enable forwarding network token cryptograms. | getIncludeCryptogram(): ?bool | setIncludeCryptogram(?bool includeCryptogram): void |
| `useNetworkToken` | `?bool` | Optional | Set to **true** to forward the network token for a card. | getUseNetworkToken(): ?bool | setUseNetworkToken(?bool useNetworkToken): void |

## Example (as JSON)

```json
{
  "includeCryptogram": false,
  "useNetworkToken": false
}
```

