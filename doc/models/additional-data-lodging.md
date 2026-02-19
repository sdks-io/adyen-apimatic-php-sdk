
# Additional Data Lodging

## Structure

`AdditionalDataLodging`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `lodgingSpecialProgramCode` | `?string` | Optional | A code that corresponds to the category of lodging charges for the payment. Possible values:<br><br>* 1: Lodging<br>* 2: No show reservation<br>* 3: Advanced deposit | getLodgingSpecialProgramCode(): ?string | setLodgingSpecialProgramCode(?string lodgingSpecialProgramCode): void |
| `lodgingCheckInDate` | `?string` | Optional | The arrival date.<br><br>* Date format: **yyyyMmDd**. For example, for 2023 April 22, **20230422**. | getLodgingCheckInDate(): ?string | setLodgingCheckInDate(?string lodgingCheckInDate): void |
| `lodgingCheckOutDate` | `?string` | Optional | The departure date.<br><br>* Date format: **yyyyMmDd**. For example, for 2023 April 22, **20230422**. | getLodgingCheckOutDate(): ?string | setLodgingCheckOutDate(?string lodgingCheckOutDate): void |
| `lodgingCustomerServiceTollFreeNumber` | `?string` | Optional | The toll-free phone number for the lodging.<br><br>* Format: numeric<br>* Max length: 17 characters.<br>* For US and CA numbers must be 10 characters in length<br>* Must not start with a space<br>* Must not contain any special characters such as + or -<br>* Must not be all zeros. | getLodgingCustomerServiceTollFreeNumber(): ?string | setLodgingCustomerServiceTollFreeNumber(?string lodgingCustomerServiceTollFreeNumber): void |
| `lodgingFireSafetyActIndicator` | `?string` | Optional | Identifies that the facility complies with the Hotel and Motel Fire Safety Act of 1990. Must be 'Y' or 'N'.<br><br>* Format: alphabetic<br>* Max length: 1 character | getLodgingFireSafetyActIndicator(): ?string | setLodgingFireSafetyActIndicator(?string lodgingFireSafetyActIndicator): void |
| `lodgingFolioCashAdvances` | `?string` | Optional | The folio cash advances, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters | getLodgingFolioCashAdvances(): ?string | setLodgingFolioCashAdvances(?string lodgingFolioCashAdvances): void |
| `lodgingFolioNumber` | `?string` | Optional | The card acceptor’s internal invoice or billing ID reference number.<br><br>* Max length: 25 characters<br>* Must not start with a space<br>* Must not contain any special characters<br>* Must not be all zeros. | getLodgingFolioNumber(): ?string | setLodgingFolioNumber(?string lodgingFolioNumber): void |
| `lodgingFoodBeverageCharges` | `?string` | Optional | Any charges for food and beverages associated with the booking, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters | getLodgingFoodBeverageCharges(): ?string | setLodgingFoodBeverageCharges(?string lodgingFoodBeverageCharges): void |
| `lodgingNoShowIndicator` | `?string` | Optional | Indicates if the customer didn't check in for their booking.<br>Possible values:<br><br>* **Y**: the customer didn't check in<br>* **N**: the customer checked in | getLodgingNoShowIndicator(): ?string | setLodgingNoShowIndicator(?string lodgingNoShowIndicator): void |
| `lodgingPrepaidExpenses` | `?string` | Optional | The prepaid expenses for the booking.<br><br>* Format: numeric<br>* Max length: 12 characters | getLodgingPrepaidExpenses(): ?string | setLodgingPrepaidExpenses(?string lodgingPrepaidExpenses): void |
| `lodgingPropertyPhoneNumber` | `?string` | Optional | The lodging property location's phone number.<br><br>* Format: numeric<br>* Min length: 10 characters<br>* Max length: 17 characters<br>* For US and CA numbers must be 10 characters in length<br>* Must not start with a space<br>* Must not contain any special characters such as + or -<br>* Must not be all zeros. | getLodgingPropertyPhoneNumber(): ?string | setLodgingPropertyPhoneNumber(?string lodgingPropertyPhoneNumber): void |
| `lodgingRoom1NumberOfNights` | `?string` | Optional | The total number of nights the room is booked for.<br><br>* Format: numeric<br>* Must be a number between 0 and 99<br>* Max length: 4 characters | getLodgingRoom1NumberOfNights(): ?string | setLodgingRoom1NumberOfNights(?string lodgingRoom1NumberOfNights): void |
| `lodgingRoom1Rate` | `?string` | Optional | The rate for the room, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number | getLodgingRoom1Rate(): ?string | setLodgingRoom1Rate(?string lodgingRoom1Rate): void |
| `lodgingTotalRoomTax` | `?string` | Optional | The total room tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number | getLodgingTotalRoomTax(): ?string | setLodgingTotalRoomTax(?string lodgingTotalRoomTax): void |
| `lodgingTotalTax` | `?string` | Optional | The total tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* Format: numeric<br>* Max length: 12 characters<br>* Must not be a negative number | getLodgingTotalTax(): ?string | setLodgingTotalTax(?string lodgingTotalTax): void |
| `travelEntertainmentAuthDataDuration` | `?string` | Optional | The number of nights. This should be included in the auth message.<br><br>* Format: numeric<br>* Max length: 4 characters | getTravelEntertainmentAuthDataDuration(): ?string | setTravelEntertainmentAuthDataDuration(?string travelEntertainmentAuthDataDuration): void |
| `travelEntertainmentAuthDataMarket` | `?string` | Optional | Indicates what market-specific dataset will be submitted. Must be 'H' for Hotel. This should be included in the auth message.<br><br>* Format: alphanumeric<br>* Max length: 1 character | getTravelEntertainmentAuthDataMarket(): ?string | setTravelEntertainmentAuthDataMarket(?string travelEntertainmentAuthDataMarket): void |

## Example (as JSON)

```json
{
  "lodging.SpecialProgramCode": "lodging.SpecialProgramCode8",
  "lodging.checkInDate": "lodging.checkInDate2",
  "lodging.checkOutDate": "lodging.checkOutDate6",
  "lodging.customerServiceTollFreeNumber": "lodging.customerServiceTollFreeNumber4",
  "lodging.fireSafetyActIndicator": "lodging.fireSafetyActIndicator4"
}
```

