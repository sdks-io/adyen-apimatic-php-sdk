
# Service Error Exception

*This model accepts additional fields of type array.*

## Structure

`ServiceErrorException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `additionalData` | `?array<string,string>` | Optional | Contains additional information about the payment. Some data fields are included only if you select them first. Go to **Customer Area** > **Developers** > **Additional data**. | getAdditionalData(): ?array | setAdditionalData(?array additionalData): void |
| `errorCode` | `?string` | Optional | The error code mapped to the error message. | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errorType` | `?string` | Optional | The category of the error. | getErrorType(): ?string | setErrorType(?string errorType): void |
| `message` | `?string` | Optional | A short explanation of the issue. | getMessage(): ?string | setMessage(?string message): void |
| `pspReference` | `?string` | Optional | The PSP reference of the payment. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `status` | `?int` | Optional | The HTTP response status. | getStatus(): ?int | setStatus(?int status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "additionalData": {
    "key0": "additionalData0"
  },
  "errorCode": "errorCode6",
  "errorType": "errorType0",
  "message": "message0",
  "pspReference": "pspReference8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

