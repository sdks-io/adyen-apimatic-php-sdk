
# Additional Data Temporary Services

## Structure

`AdditionalDataTemporaryServices`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enhancedSchemeDataCustomerReference` | `?string` | Optional | The customer code, if supplied by a customer.<br><br>* Encoding: ASCII<br>* maxLength: 25 | getEnhancedSchemeDataCustomerReference(): ?string | setEnhancedSchemeDataCustomerReference(?string enhancedSchemeDataCustomerReference): void |
| `enhancedSchemeDataEmployeeName` | `?string` | Optional | The name or ID of the person working in a temporary capacity.<br><br>* maxLength: 40.<br>* Must not be all spaces.<br>  *Must not be all zeros. | getEnhancedSchemeDataEmployeeName(): ?string | setEnhancedSchemeDataEmployeeName(?string enhancedSchemeDataEmployeeName): void |
| `enhancedSchemeDataJobDescription` | `?string` | Optional | The job description of the person working in a temporary capacity.<br><br>* maxLength: 40<br>* Must not be all spaces.<br>  *Must not be all zeros. | getEnhancedSchemeDataJobDescription(): ?string | setEnhancedSchemeDataJobDescription(?string enhancedSchemeDataJobDescription): void |
| `enhancedSchemeDataRegularHoursRate` | `?string` | Optional | The amount paid for regular hours worked, [minor units](https://docs.adyen.com/development-resources/currency-codes).<br><br>* maxLength: 7<br>* Must not be empty<br>* Can be all zeros | getEnhancedSchemeDataRegularHoursRate(): ?string | setEnhancedSchemeDataRegularHoursRate(?string enhancedSchemeDataRegularHoursRate): void |
| `enhancedSchemeDataRegularHoursWorked` | `?string` | Optional | The hours worked.<br><br>* maxLength: 7<br>* Must not be empty<br>* Can be all zeros | getEnhancedSchemeDataRegularHoursWorked(): ?string | setEnhancedSchemeDataRegularHoursWorked(?string enhancedSchemeDataRegularHoursWorked): void |
| `enhancedSchemeDataRequestName` | `?string` | Optional | The name of the person requesting temporary services.<br><br>* maxLength: 40<br>* Must not be all zeros<br>* Must not be all spaces | getEnhancedSchemeDataRequestName(): ?string | setEnhancedSchemeDataRequestName(?string enhancedSchemeDataRequestName): void |
| `enhancedSchemeDataTempStartDate` | `?string` | Optional | The billing period start date.<br><br>* Format: ddMMyy<br>* maxLength: 6 | getEnhancedSchemeDataTempStartDate(): ?string | setEnhancedSchemeDataTempStartDate(?string enhancedSchemeDataTempStartDate): void |
| `enhancedSchemeDataTempWeekEnding` | `?string` | Optional | The billing period end date.<br><br>* Format: ddMMyy<br>* maxLength: 6 | getEnhancedSchemeDataTempWeekEnding(): ?string | setEnhancedSchemeDataTempWeekEnding(?string enhancedSchemeDataTempWeekEnding): void |
| `enhancedSchemeDataTotalTaxAmount` | `?string` | Optional | The total tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes). For example, 2000 means USD 20.00<br><br>* maxLength: 12 | getEnhancedSchemeDataTotalTaxAmount(): ?string | setEnhancedSchemeDataTotalTaxAmount(?string enhancedSchemeDataTotalTaxAmount): void |

## Example (as JSON)

```json
{
  "enhancedSchemeData.customerReference": "enhancedSchemeData.customerReference4",
  "enhancedSchemeData.employeeName": "enhancedSchemeData.employeeName4",
  "enhancedSchemeData.jobDescription": "enhancedSchemeData.jobDescription4",
  "enhancedSchemeData.regularHoursRate": "enhancedSchemeData.regularHoursRate8",
  "enhancedSchemeData.regularHoursWorked": "enhancedSchemeData.regularHoursWorked8"
}
```

