
# Passenger

## Structure

`Passenger`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dateOfBirth` | `?DateTime` | Optional | The passenger's date of birth.<br><br>* Format `yyyy-MM-dd`<br>* minLength: 10<br>* maxLength: 10 | getDateOfBirth(): ?\DateTime | setDateOfBirth(?\DateTime dateOfBirth): void |
| `firstName` | `?string` | Optional | The passenger's first name.<br><br>> This field is required if the airline data includes passenger details or leg details.<br><br>* Encoding: ASCII | getFirstName(): ?string | setFirstName(?string firstName): void |
| `lastName` | `?string` | Optional | The passenger's last name.<br><br>> This field is required if the airline data includes passenger details or leg details.<br><br>* Encoding: ASCII | getLastName(): ?string | setLastName(?string lastName): void |
| `phoneNumber` | `?string` | Optional | The passenger's phone number, including country code. This is an alphanumeric field that can include the '+' and '-' signs.<br><br>* Encoding: ASCII<br>* minLength: 3 characters<br>* maxLength: 30 characters | getPhoneNumber(): ?string | setPhoneNumber(?string phoneNumber): void |
| `travellerType` | `?string` | Optional | The IATA passenger type code (PTC).<br><br>* Encoding: ASCII<br>* minLength: 3 characters<br>* maxLength: 6 characters | getTravellerType(): ?string | setTravellerType(?string travellerType): void |

## Example (as JSON)

```json
{
  "dateOfBirth": "2016-03-13",
  "firstName": "firstName8",
  "lastName": "lastName0",
  "phoneNumber": "phoneNumber4",
  "travellerType": "travellerType4"
}
```

