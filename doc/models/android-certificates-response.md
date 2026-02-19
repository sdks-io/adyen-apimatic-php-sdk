
# Android Certificates Response

## Structure

`AndroidCertificatesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(AndroidCertificate[])`](../../doc/models/android-certificate.md) | Optional | Uploaded Android certificates for Android payment terminals. | getData(): ?array | setData(?array data): void |

## Example (as JSON)

```json
{
  "data": [
    {
      "description": "description0",
      "extension": "extension6",
      "id": "id0",
      "name": "name0",
      "notAfter": "2016-03-13T12:52:32.123Z",
      "notBefore": "2016-03-13T12:52:32.123Z"
    }
  ]
}
```

