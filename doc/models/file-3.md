
# File 3

For `eap` **tls**. The RSA private key for the client. Include the lines BEGIN RSA PRIVATE KEY and END RSA PRIVATE KEY.

## Structure

`File3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | `string` | Required | The certificate content converted to a Base64-encoded string. | getData(): string | setData(string data): void |
| `name` | `string` | Required | The name of the certificate. Must be unique across Wi-Fi profiles. | getName(): string | setName(string name): void |

## Example (as JSON)

```json
{
  "data": "data2",
  "name": "name2"
}
```

