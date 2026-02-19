
# Install Android Certificate Details

## Structure

`InstallAndroidCertificateDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateId` | `?string` | Optional | The unique identifier of the certificate to be installed. | getCertificateId(): ?string | setCertificateId(?string certificateId): void |
| `type` | [`?string(Type37)`](../../doc/models/type-37.md) | Optional | Type of terminal action: Install an Android certificate.<br><br>**Default**: `Type37::INSTALLANDROIDCERTIFICATE` | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "type": "InstallAndroidCertificate",
  "certificateId": "certificateId6"
}
```

