
# Airline

## Structure

`Airline`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `agency` | [`?Agency`](../../doc/models/agency.md) | Optional | - | getAgency(): ?Agency | setAgency(?Agency agency): void |
| `boardingFee` | `?int` | Optional | The amount charged for boarding the plane, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Encoding: Numeric<br>* minLength: 1 character<br>* maxLength: 11 characters | getBoardingFee(): ?int | setBoardingFee(?int boardingFee): void |
| `code` | `?string` | Optional | The [IATA](https://www.iata.org/services/pages/codes.aspx) 3-digit accounting code (PAX) that identifies the carrier.<br><br>* Format: IATA 3-digit accounting code (PAX)<br>* Example: KLM = 074<br>* minLength: 3 characters<br>* maxLength: 3 characters<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. | getCode(): ?string | setCode(?string code): void |
| `computerizedReservationSystem` | `?string` | Optional | The [CRS](https://en.wikipedia.org/wiki/Computer_reservation_system) used to make the reservation and purchase the ticket.<br><br>* Encoding: ASCII<br>* minLength: 4 characters<br>* maxLength: 4 characters | getComputerizedReservationSystem(): ?string | setComputerizedReservationSystem(?string computerizedReservationSystem): void |
| `customerReferenceNumber` | `?string` | Optional | The alphanumeric customer reference number.<br><br>* Encoding: ASCII<br>* maxLength: 20 characters<br>* If you send more than 20 characters, the customer reference number is truncated<br>* Must not start with a space or be all spaces. | getCustomerReferenceNumber(): ?string | setCustomerReferenceNumber(?string customerReferenceNumber): void |
| `designatorCode` | `?string` | Optional | The [IATA](https://www.iata.org/services/pages/codes.aspx) 2-letter accounting code (PAX) that identifies the carrier.<br><br>* Encoding: ASCII<br>* Example: KLM = KL<br>* minLength: 2 characters<br>* maxLength: 2 characters<br>* Must not start with a space or be all spaces. | getDesignatorCode(): ?string | setDesignatorCode(?string designatorCode): void |
| `documentType` | `?string` | Optional | A code that identifies the type of item bought. The description of the code can appear on credit card statements.<br><br>* Encoding: ASCII<br>* Example: Passenger ticket = 01<br>* minLength: 2 characters<br>* maxLength: 2 characters | getDocumentType(): ?string | setDocumentType(?string documentType): void |
| `flightDate` | `?DateTime` | Optional | The flight departure date. Time is optional.<br><br>* Format for date only: `yyyy-MM-dd`<br>* Format for date and time: `yyyy-MM-ddTHH:mm`<br>* Use local time of departure airport.<br>* minLength: 10 characters<br>* maxLength: 16 characters | getFlightDate(): ?\DateTime | setFlightDate(?\DateTime flightDate): void |
| `legs` | [`?(Leg[])`](../../doc/models/leg.md) | Optional | - | getLegs(): ?array | setLegs(?array legs): void |
| `passengerName` | `string` | Required | The passenger's name, initials, and title.<br><br>* Format: last name + first name or initials + title<br>* Example: *FLYER / MARY MS*<br>* minLength: 1 character<br>* maxLength: 20 characters<br>* If you send more than 20 characters, the name is truncated<br>* Must not start with a space or be all spaces.<br>* Must not be all zeros. | getPassengerName(): string | setPassengerName(string passengerName): void |
| `passengers` | [`?(Passenger[])`](../../doc/models/passenger.md) | Optional | - | getPassengers(): ?array | setPassengers(?array passengers): void |
| `ticket` | [`?Ticket`](../../doc/models/ticket.md) | Optional | - | getTicket(): ?Ticket | setTicket(?Ticket ticket): void |
| `travelAgency` | [`?TravelAgency`](../../doc/models/travel-agency.md) | Optional | - | getTravelAgency(): ?TravelAgency | setTravelAgency(?TravelAgency travelAgency): void |

## Example (as JSON)

```json
{
  "agency": {
    "invoiceNumber": "invoiceNumber6",
    "planName": "planName6"
  },
  "boardingFee": 186,
  "code": "code6",
  "computerizedReservationSystem": "computerizedReservationSystem8",
  "customerReferenceNumber": "customerReferenceNumber0",
  "passengerName": "passengerName6"
}
```

