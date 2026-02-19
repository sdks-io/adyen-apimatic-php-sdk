
# Response Additional Data Installments

## Structure

`ResponseAdditionalDataInstallments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `installmentPaymentDataInstallmentType` | `?string` | Optional | Type of installment. The value of `installmentType` should be **IssuerFinanced**. | getInstallmentPaymentDataInstallmentType(): ?string | setInstallmentPaymentDataInstallmentType(?string installmentPaymentDataInstallmentType): void |
| `installmentPaymentDataOptionItemNrAnnualPercentageRate` | `?string` | Optional | Annual interest rate. | getInstallmentPaymentDataOptionItemNrAnnualPercentageRate(): ?string | setInstallmentPaymentDataOptionItemNrAnnualPercentageRate(?string installmentPaymentDataOptionItemNrAnnualPercentageRate): void |
| `installmentPaymentDataOptionItemNrFirstInstallmentAmount` | `?string` | Optional | First Installment Amount in minor units. | getInstallmentPaymentDataOptionItemNrFirstInstallmentAmount(): ?string | setInstallmentPaymentDataOptionItemNrFirstInstallmentAmount(?string installmentPaymentDataOptionItemNrFirstInstallmentAmount): void |
| `installmentPaymentDataOptionItemNrInstallmentFee` | `?string` | Optional | Installment fee amount in minor units. | getInstallmentPaymentDataOptionItemNrInstallmentFee(): ?string | setInstallmentPaymentDataOptionItemNrInstallmentFee(?string installmentPaymentDataOptionItemNrInstallmentFee): void |
| `installmentPaymentDataOptionItemNrInterestRate` | `?string` | Optional | Interest rate for the installment period. | getInstallmentPaymentDataOptionItemNrInterestRate(): ?string | setInstallmentPaymentDataOptionItemNrInterestRate(?string installmentPaymentDataOptionItemNrInterestRate): void |
| `installmentPaymentDataOptionItemNrMaximumNumberOfInstallments` | `?string` | Optional | Maximum number of installments possible for this payment. | getInstallmentPaymentDataOptionItemNrMaximumNumberOfInstallments(): ?string | setInstallmentPaymentDataOptionItemNrMaximumNumberOfInstallments(?string installmentPaymentDataOptionItemNrMaximumNumberOfInstallments): void |
| `installmentPaymentDataOptionItemNrMinimumNumberOfInstallments` | `?string` | Optional | Minimum number of installments possible for this payment. | getInstallmentPaymentDataOptionItemNrMinimumNumberOfInstallments(): ?string | setInstallmentPaymentDataOptionItemNrMinimumNumberOfInstallments(?string installmentPaymentDataOptionItemNrMinimumNumberOfInstallments): void |
| `installmentPaymentDataOptionItemNrNumberOfInstallments` | `?string` | Optional | Total number of installments possible for this payment. | getInstallmentPaymentDataOptionItemNrNumberOfInstallments(): ?string | setInstallmentPaymentDataOptionItemNrNumberOfInstallments(?string installmentPaymentDataOptionItemNrNumberOfInstallments): void |
| `installmentPaymentDataOptionItemNrSubsequentInstallmentAmount` | `?string` | Optional | Subsequent Installment Amount in minor units. | getInstallmentPaymentDataOptionItemNrSubsequentInstallmentAmount(): ?string | setInstallmentPaymentDataOptionItemNrSubsequentInstallmentAmount(?string installmentPaymentDataOptionItemNrSubsequentInstallmentAmount): void |
| `installmentPaymentDataOptionItemNrTotalAmountDue` | `?string` | Optional | Total amount in minor units. | getInstallmentPaymentDataOptionItemNrTotalAmountDue(): ?string | setInstallmentPaymentDataOptionItemNrTotalAmountDue(?string installmentPaymentDataOptionItemNrTotalAmountDue): void |
| `installmentPaymentDataPaymentOptions` | `?string` | Optional | Possible values:<br><br>* PayInInstallmentsOnly<br>* PayInFullOnly<br>* PayInFullOrInstallments | getInstallmentPaymentDataPaymentOptions(): ?string | setInstallmentPaymentDataPaymentOptions(?string installmentPaymentDataPaymentOptions): void |
| `installmentsValue` | `?string` | Optional | The number of installments that the payment amount should be charged with.<br><br>Example: 5<br><br>> Only relevant for card payments in countries that support installments. | getInstallmentsValue(): ?string | setInstallmentsValue(?string installmentsValue): void |

## Example (as JSON)

```json
{
  "installmentPaymentData.installmentType": "installmentPaymentData.installmentType8",
  "installmentPaymentData.option[itemNr].annualPercentageRate": "installmentPaymentData.option[itemNr].annualPercentageRate2",
  "installmentPaymentData.option[itemNr].firstInstallmentAmount": "installmentPaymentData.option[itemNr].firstInstallmentAmount6",
  "installmentPaymentData.option[itemNr].installmentFee": "installmentPaymentData.option[itemNr].installmentFee8",
  "installmentPaymentData.option[itemNr].interestRate": "installmentPaymentData.option[itemNr].interestRate4"
}
```

