
# Additional Data Car Rental

## Structure

`AdditionalDataCarRental`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `carRentalCheckOutDate` | `?string` | Optional | The pick-up date.<br><br>* Date format: `yyyyMMdd` | getCarRentalCheckOutDate(): ?string | setCarRentalCheckOutDate(?string carRentalCheckOutDate): void |
| `carRentalCustomerServiceTollFreeNumber` | `?string` | Optional | The customer service phone number of the car rental company.<br><br>* Format: Alphanumeric<br>* maxLength: 17<br>* For US and CA numbers must be 10 characters in length<br>* Must not start with a space<br>* Must not contain any special characters such as + or -<br>  *Must not be all zeros. | getCarRentalCustomerServiceTollFreeNumber(): ?string | setCarRentalCustomerServiceTollFreeNumber(?string carRentalCustomerServiceTollFreeNumber): void |
| `carRentalDaysRented` | `?string` | Optional | Number of days for which the car is being rented.<br><br>* Format: Numeric<br>* maxLength: 4<br>* Must not be all spaces | getCarRentalDaysRented(): ?string | setCarRentalDaysRented(?string carRentalDaysRented): void |
| `carRentalFuelCharges` | `?string` | Optional | Any fuel charges associated with the rental, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: Numeric<br>* maxLength: 12 | getCarRentalFuelCharges(): ?string | setCarRentalFuelCharges(?string carRentalFuelCharges): void |
| `carRentalInsuranceCharges` | `?string` | Optional | Any insurance charges associated with the rental, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: Numeric<br>* maxLength: 12<br>* Must not be all spaces<br>  *Must not be all zeros. | getCarRentalInsuranceCharges(): ?string | setCarRentalInsuranceCharges(?string carRentalInsuranceCharges): void |
| `carRentalLocationCity` | `?string` | Optional | The city where the car is rented.<br><br>* Format: Alphanumeric<br>* maxLength: 18<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalLocationCity(): ?string | setCarRentalLocationCity(?string carRentalLocationCity): void |
| `carRentalLocationCountry` | `?string` | Optional | The country where the car is rented, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format.<br><br>* Format: Alphanumeric<br>* maxLength: 2 | getCarRentalLocationCountry(): ?string | setCarRentalLocationCountry(?string carRentalLocationCountry): void |
| `carRentalLocationStateProvince` | `?string` | Optional | The state or province where the car is rented.<br><br>* Format: Alphanumeric<br>* maxLength: 2<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalLocationStateProvince(): ?string | setCarRentalLocationStateProvince(?string carRentalLocationStateProvince): void |
| `carRentalNoShowIndicator` | `?string` | Optional | Indicates if the customer didn't pick up their rental car.<br><br>* Y - Customer did not pick up their car<br>* N - Not applicable | getCarRentalNoShowIndicator(): ?string | setCarRentalNoShowIndicator(?string carRentalNoShowIndicator): void |
| `carRentalOneWayDropOffCharges` | `?string` | Optional | The charge for not returning a car to the original rental location, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* maxLength: 12 | getCarRentalOneWayDropOffCharges(): ?string | setCarRentalOneWayDropOffCharges(?string carRentalOneWayDropOffCharges): void |
| `carRentalRate` | `?string` | Optional | The daily rental rate, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: Alphanumeric<br>* maxLength: 12 | getCarRentalRate(): ?string | setCarRentalRate(?string carRentalRate): void |
| `carRentalRateIndicator` | `?string` | Optional | Specifies whether the given rate is applied daily or weekly.<br><br>* D - Daily rate<br>* W - Weekly rate | getCarRentalRateIndicator(): ?string | setCarRentalRateIndicator(?string carRentalRateIndicator): void |
| `carRentalRentalAgreementNumber` | `?string` | Optional | The rental agreement number for the car rental.<br><br>* Format: Alphanumeric<br>* maxLength: 9<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalRentalAgreementNumber(): ?string | setCarRentalRentalAgreementNumber(?string carRentalRentalAgreementNumber): void |
| `carRentalRentalClassId` | `?string` | Optional | The classification of the rental car.<br><br>* Format: Alphanumeric<br>* maxLength: 4<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalRentalClassId(): ?string | setCarRentalRentalClassId(?string carRentalRentalClassId): void |
| `carRentalRenterName` | `?string` | Optional | The name of the person renting the car.<br><br>* Format: Alphanumeric<br>* maxLength: 26<br>* If you send more than 26 characters, the name is truncated<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalRenterName(): ?string | setCarRentalRenterName(?string carRentalRenterName): void |
| `carRentalReturnCity` | `?string` | Optional | The city where the car must be returned.<br><br>* Format: Alphanumeric<br>* maxLength: 18<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalReturnCity(): ?string | setCarRentalReturnCity(?string carRentalReturnCity): void |
| `carRentalReturnCountry` | `?string` | Optional | The country where the car must be returned, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format.<br><br>* Format: Alphanumeric<br>* maxLength: 2 | getCarRentalReturnCountry(): ?string | setCarRentalReturnCountry(?string carRentalReturnCountry): void |
| `carRentalReturnDate` | `?string` | Optional | The last date to return the car by.<br><br>* Date format: `yyyyMMdd`<br>* maxLength: 8 | getCarRentalReturnDate(): ?string | setCarRentalReturnDate(?string carRentalReturnDate): void |
| `carRentalReturnLocationId` | `?string` | Optional | The agency code, phone number, or address abbreviation<br><br>* Format: Alphanumeric<br>* maxLength: 10<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalReturnLocationId(): ?string | setCarRentalReturnLocationId(?string carRentalReturnLocationId): void |
| `carRentalReturnStateProvince` | `?string` | Optional | The state or province where the car must be returned.<br><br>* Format: Alphanumeric<br>* maxLength: 3<br>* Must not start with a space or be all spaces<br>  *Must not be all zeros. | getCarRentalReturnStateProvince(): ?string | setCarRentalReturnStateProvince(?string carRentalReturnStateProvince): void |
| `carRentalTaxExemptIndicator` | `?string` | Optional | Indicates if the goods or services were tax-exempt, or if tax was not paid on them.<br><br>Values:<br><br>* Y - Goods or services were tax exempt<br>* N - Tax was not collected | getCarRentalTaxExemptIndicator(): ?string | setCarRentalTaxExemptIndicator(?string carRentalTaxExemptIndicator): void |
| `travelEntertainmentAuthDataDuration` | `?string` | Optional | Number of days the car is rented for. This should be included in the auth message.<br><br>* Format: Numeric<br>* maxLength: 4 | getTravelEntertainmentAuthDataDuration(): ?string | setTravelEntertainmentAuthDataDuration(?string travelEntertainmentAuthDataDuration): void |
| `travelEntertainmentAuthDataMarket` | `?string` | Optional | Indicates what market-specific dataset will be submitted or is being submitted. Value should be 'A' for car rental. This should be included in the auth message.<br><br>* Format: Alphanumeric<br>* maxLength: 1 | getTravelEntertainmentAuthDataMarket(): ?string | setTravelEntertainmentAuthDataMarket(?string travelEntertainmentAuthDataMarket): void |

## Example (as JSON)

```json
{
  "carRental.checkOutDate": "carRental.checkOutDate4",
  "carRental.customerServiceTollFreeNumber": "carRental.customerServiceTollFreeNumber6",
  "carRental.daysRented": "carRental.daysRented8",
  "carRental.fuelCharges": "carRental.fuelCharges6",
  "carRental.insuranceCharges": "carRental.insuranceCharges6"
}
```

