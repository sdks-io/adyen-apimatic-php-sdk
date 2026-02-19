
# Payment Validations Name Result Raw Response 2

Contains the raw response(s) returned by the scheme for the name validation.

## Structure

`PaymentValidationsNameResultRawResponse2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firstName` | `?string` | Optional | The raw first name validation result that Adyen received from the scheme. First name validation result is only returned for Visa. | getFirstName(): ?string | setFirstName(?string firstName): void |
| `fullName` | `?string` | Optional | The raw full name validation result that Adyen received from the scheme. Full name is the only field that is validated for Mastercard | getFullName(): ?string | setFullName(?string fullName): void |
| `lastName` | `?string` | Optional | The raw last name validation result that Adyen received from the scheme. Last name validation result is only returned for Visa. | getLastName(): ?string | setLastName(?string lastName): void |
| `middleName` | `?string` | Optional | The raw middle name validation result that Adyen received from the scheme. Middle name validation result is only returned for Visa. | getMiddleName(): ?string | setMiddleName(?string middleName): void |
| `status` | `?string` | Optional | The raw name validation status value that Adyen received from the scheme. Only returned for Visa. | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
{
  "firstName": "firstName8",
  "fullName": "fullName6",
  "lastName": "lastName0",
  "middleName": "middleName4",
  "status": "status2"
}
```

