
# Payment Method Upi Apps

## Structure

`PaymentMethodUpiApps`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `string` | Required | The unique identifier of this app, to submit in requests to /payments. | getId(): string | setId(string id): void |
| `name` | `string` | Required | A localized name of the app. | getName(): string | setName(string name): void |

## Example (as JSON)

```json
{
  "id": "id8",
  "name": "name8"
}
```

