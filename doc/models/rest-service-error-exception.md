
# Rest Service Error Exception

*This model accepts additional fields of type array.*

## Structure

`RestServiceErrorException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `detail` | `string` | Required | A human-readable explanation specific to this occurrence of the problem. | getDetail(): string | setDetail(string detail): void |
| `errorCode` | `string` | Required | A code that identifies the problem type. | getErrorCode(): string | setErrorCode(string errorCode): void |
| `instance` | `?string` | Optional | A unique URI that identifies the specific occurrence of the problem. | getInstance(): ?string | setInstance(?string instance): void |
| `invalidFields` | [`?(InvalidField[])`](../../doc/models/invalid-field.md) | Optional | Detailed explanation of each validation error, when applicable. | getInvalidFields(): ?array | setInvalidFields(?array invalidFields): void |
| `requestId` | `?string` | Optional | A unique reference for the request, essentially the same as `pspReference`. | getRequestId(): ?string | setRequestId(?string requestId): void |
| `response` | `?array` | Optional | JSON response payload. | getResponse(): ?array | setResponse(?array response): void |
| `status` | `int` | Required | The HTTP status code. | getStatus(): int | setStatus(int status): void |
| `title` | `string` | Required | A short, human-readable summary of the problem type. | getTitle(): string | setTitle(string title): void |
| `type` | `string` | Required | A URI that identifies the problem type, pointing to human-readable documentation on this problem type. | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "detail": "detail8",
  "errorCode": "errorCode8",
  "instance": "instance8",
  "invalidFields": [
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
  "requestId": "requestId4",
  "response": {
    "key1": "val1",
    "key2": "val2"
  },
  "status": 158,
  "title": "title8",
  "type": "type2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

