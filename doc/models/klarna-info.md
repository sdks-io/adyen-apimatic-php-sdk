
# Klarna Info

## Structure

`KlarnaInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoCapture` | `?bool` | Optional | Indicates the status of [Automatic capture](https://docs.adyen.com/online-payments/capture#automatic-capture). Default value: **false**. | getAutoCapture(): ?bool | setAutoCapture(?bool autoCapture): void |
| `disputeEmail` | `string` | Required | The email address for disputes. | getDisputeEmail(): string | setDisputeEmail(string disputeEmail): void |
| `region` | [`string(Region)`](../../doc/models/region.md) | Required | The region of operation. For example, **NA**, **EU**, **CH**, **AU**.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` | getRegion(): string | setRegion(string region): void |
| `supportEmail` | `string` | Required | The email address of merchant support. | getSupportEmail(): string | setSupportEmail(string supportEmail): void |

## Example (as JSON)

```json
{
  "autoCapture": false,
  "disputeEmail": "disputeEmail8",
  "region": "CH",
  "supportEmail": "supportEmail2"
}
```

