
# Android Certificate

## Structure

`AndroidCertificate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | The description that was provided when uploading the certificate. | getDescription(): ?string | setDescription(?string description): void |
| `extension` | `?string` | Optional | The file format of the certificate, as indicated by the file extension. For example, **.cert** or **.pem**. | getExtension(): ?string | setExtension(?string extension): void |
| `id` | `string` | Required | The unique identifier of the certificate. | getId(): string | setId(string id): void |
| `name` | `?string` | Optional | The file name of the certificate. For example, **mycert**. | getName(): ?string | setName(?string name): void |
| `notAfter` | `?DateTime` | Optional | The date when the certificate stops to be valid. | getNotAfter(): ?\DateTime | setNotAfter(?\DateTime notAfter): void |
| `notBefore` | `?DateTime` | Optional | The date when the certificate starts to be valid. | getNotBefore(): ?\DateTime | setNotBefore(?\DateTime notBefore): void |
| `status` | `?string` | Optional | The status of the certificate. | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
{
  "description": "description8",
  "extension": "extension4",
  "id": "id8",
  "name": "name8",
  "notAfter": "2016-03-13T12:52:32.123Z",
  "notBefore": "2016-03-13T12:52:32.123Z"
}
```

