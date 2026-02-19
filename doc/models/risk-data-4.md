
# Risk Data 4

Contains risk data, such as client-side data, used to identify risk for a transaction.

## Structure

`RiskData4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `clientData` | `?string` | Optional | Contains client-side data, like the device fingerprint, cookies, and specific browser settings.<br><br>**Constraints**: *Maximum Length*: `5000` | getClientData(): ?string | setClientData(?string clientData): void |
| `customFields` | `?array<string,string>` | Optional | Any custom fields used as part of the input to configured risk rules. | getCustomFields(): ?array | setCustomFields(?array customFields): void |
| `fraudOffset` | `?int` | Optional | An integer value that is added to the normal fraud score. The value can be either positive or negative. | getFraudOffset(): ?int | setFraudOffset(?int fraudOffset): void |
| `profileReference` | `?string` | Optional | The risk profile to assign to this payment. When left empty, the merchant-level account's default risk profile will be applied. | getProfileReference(): ?string | setProfileReference(?string profileReference): void |

## Example (as JSON)

```json
{
  "clientData": "clientData2",
  "customFields": {
    "key0": "customFields0",
    "key1": "customFields1"
  },
  "fraudOffset": 166,
  "profileReference": "profileReference0"
}
```

