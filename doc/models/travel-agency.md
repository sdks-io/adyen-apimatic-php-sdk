
# Travel Agency

## Structure

`TravelAgency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | `?string` | Optional | The unique identifier from IATA or ARC for the travel agency that issues the ticket.<br><br>* Encoding: ASCII<br>* minLength: 1 character<br>* maxLength: 8 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. | getCode(): ?string | setCode(?string code): void |
| `name` | `?string` | Optional | The name of the travel agency.<br><br>* Encoding: ASCII<br>* minLength: 1 character<br>* maxLength: 25 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. | getName(): ?string | setName(?string name): void |

## Example (as JSON)

```json
{
  "code": "code4",
  "name": "name6"
}
```

