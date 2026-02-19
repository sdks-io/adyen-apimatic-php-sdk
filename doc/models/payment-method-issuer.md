
# Payment Method Issuer

## Structure

`PaymentMethodIssuer`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `disabled` | `?bool` | Optional | A boolean value indicating whether this issuer is unavailable. Can be `true` whenever the issuer is offline.<br><br>**Default**: `false` | getDisabled(): ?bool | setDisabled(?bool disabled): void |
| `id` | `string` | Required | The unique identifier of this issuer, to submit in requests to /payments. | getId(): string | setId(string id): void |
| `name` | `string` | Required | A localized name of the issuer. | getName(): string | setName(string name): void |

## Example (as JSON)

```json
{
  "disabled": false,
  "id": "id2",
  "name": "name2"
}
```

