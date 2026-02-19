
# Payment Validations Name Result Response

## Structure

`PaymentValidationsNameResultResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firstName` | `?string` | Optional | Informs you if the first name your shopper provided matches the cardholder first name on file at the issuing bank. The first name is only validated for Visa. Possible values:<br><br>**match**, **partialMatch**, **noMatch** | getFirstName(): ?string | setFirstName(?string firstName): void |
| `fullName` | `?string` | Optional | Informs you if the full name your shopper provided matches the cardholder name on file at the issuing bank. The full name is the only field that is validated for Mastercard. Possible values:<br><br>**match**, **partialMatch**, **noMatch** | getFullName(): ?string | setFullName(?string fullName): void |
| `lastName` | `?string` | Optional | Informs you if the last name your shopper provided matches the cardholder last name on file at the issuing bank. The last name is only validated for Visa. Possible values:<br><br>**match**, **partialMatch**, **noMatch** | getLastName(): ?string | setLastName(?string lastName): void |
| `middleName` | `?string` | Optional | Informs you if the middle name your shopper provided matches the cardholder middle name on file at the issuing bank. The middle name is only validated for Visa. Possible values:<br><br>**match**, **partialMatch**, **noMatch** | getMiddleName(): ?string | setMiddleName(?string middleName): void |

## Example (as JSON)

```json
{
  "firstName": "firstName4",
  "fullName": "fullName0",
  "lastName": "lastName4",
  "middleName": "middleName8"
}
```

