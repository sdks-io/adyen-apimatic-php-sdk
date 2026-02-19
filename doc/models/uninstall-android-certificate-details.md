
# Uninstall Android Certificate Details

*This model accepts additional fields of type array.*

## Structure

`UninstallAndroidCertificateDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateId` | `?string` | Optional | The unique identifier of the certificate to be uninstalled. | getCertificateId(): ?string | setCertificateId(?string certificateId): void |
| `type` | [`?string(Type71)`](../../doc/models/type-71.md) | Optional | Type of terminal action: Uninstall an Android certificate.<br><br>**Default**: `Type71::UNINSTALLANDROIDCERTIFICATE` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "UninstallAndroidCertificate",
  "certificateId": "certificateId6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

