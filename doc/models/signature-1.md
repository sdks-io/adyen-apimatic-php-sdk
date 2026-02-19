
# Signature 1

Settings to skip signature, sign on display, or sign on receipt.

## Structure

`Signature1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `askSignatureOnScreen` | `?bool` | Optional | If `skipSignature` is false, indicates whether the shopper should provide a signature on the display (**true**) or on the merchant receipt (**false**). | getAskSignatureOnScreen(): ?bool | setAskSignatureOnScreen(?bool askSignatureOnScreen): void |
| `deviceName` | `?string` | Optional | Name that identifies the terminal. | getDeviceName(): ?string | setDeviceName(?string deviceName): void |
| `deviceSlogan` | `?string` | Optional | Slogan shown on the start screen of the device.<br><br>**Constraints**: *Maximum Length*: `50` | getDeviceSlogan(): ?string | setDeviceSlogan(?string deviceSlogan): void |
| `skipSignature` | `?bool` | Optional | Skip asking for a signature. This is possible because all global card schemes (American Express, Diners, Discover, JCB, MasterCard, VISA, and UnionPay) regard a signature as optional. | getSkipSignature(): ?bool | setSkipSignature(?bool skipSignature): void |

## Example (as JSON)

```json
{
  "askSignatureOnScreen": false,
  "deviceName": "deviceName2",
  "deviceSlogan": "deviceSlogan0",
  "skipSignature": false
}
```

