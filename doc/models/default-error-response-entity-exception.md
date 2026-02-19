
# Default Error Response Entity Exception

Standardized error response following RFC-7807 format

Find out more here: [https://www.rfc-editor.org/rfc/rfc7807](https://www.rfc-editor.org/rfc/rfc7807)

*This model accepts additional fields of type array.*

## Structure

`DefaultErrorResponseEntityException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `detail` | `?string` | Optional | A human-readable explanation specific to this occurrence of the problem. | getDetail(): ?string | setDetail(?string detail): void |
| `errorCode` | `?string` | Optional | Unique business error code. | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `instance` | `?string` | Optional | A URI that identifies the specific occurrence of the problem if applicable. | getInstance(): ?string | setInstance(?string instance): void |
| `invalidFields` | [`?(InvalidField[])`](../../doc/models/invalid-field.md) | Optional | Array of fields with validation errors when applicable. | getInvalidFields(): ?array | setInvalidFields(?array invalidFields): void |
| `requestId` | `?string` | Optional | The unique reference for the request. | getRequestId(): ?string | setRequestId(?string requestId): void |
| `status` | `?int` | Optional | The HTTP status code. | getStatus(): ?int | setStatus(?int status): void |
| `title` | `?string` | Optional | A short, human-readable summary of the problem type. | getTitle(): ?string | setTitle(?string title): void |
| `type` | `?string` | Optional | A URI that identifies the validation error type. It points to human-readable documentation for the problem type. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "detail": "detail0",
  "errorCode": "errorCode0",
  "instance": "instance0",
  "invalidFields": [
    {
      "name": "name6",
      "value": "value8",
      "message": "message6",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "name": "name6",
      "value": "value8",
      "message": "message6",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "requestId": "requestId6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

