
# Additional Data Ratepay

## Structure

`AdditionalDataRatepay`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ratepayInstallmentAmount` | `?string` | Optional | Amount the customer has to pay each month. | getRatepayInstallmentAmount(): ?string | setRatepayInstallmentAmount(?string ratepayInstallmentAmount): void |
| `ratepayInterestRate` | `?string` | Optional | Interest rate of this installment. | getRatepayInterestRate(): ?string | setRatepayInterestRate(?string ratepayInterestRate): void |
| `ratepayLastInstallmentAmount` | `?string` | Optional | Amount of the last installment. | getRatepayLastInstallmentAmount(): ?string | setRatepayLastInstallmentAmount(?string ratepayLastInstallmentAmount): void |
| `ratepayPaymentFirstday` | `?string` | Optional | Calendar day of the first payment. | getRatepayPaymentFirstday(): ?string | setRatepayPaymentFirstday(?string ratepayPaymentFirstday): void |
| `ratepaydataDeliveryDate` | `?string` | Optional | Date the merchant delivered the goods to the customer. | getRatepaydataDeliveryDate(): ?string | setRatepaydataDeliveryDate(?string ratepaydataDeliveryDate): void |
| `ratepaydataDueDate` | `?string` | Optional | Date by which the customer must settle the payment. | getRatepaydataDueDate(): ?string | setRatepaydataDueDate(?string ratepaydataDueDate): void |
| `ratepaydataInvoiceDate` | `?string` | Optional | Invoice date, defined by the merchant. If not included, the invoice date is set to the delivery date. | getRatepaydataInvoiceDate(): ?string | setRatepaydataInvoiceDate(?string ratepaydataInvoiceDate): void |
| `ratepaydataInvoiceId` | `?string` | Optional | Identification name or number for the invoice, defined by the merchant. | getRatepaydataInvoiceId(): ?string | setRatepaydataInvoiceId(?string ratepaydataInvoiceId): void |

## Example (as JSON)

```json
{
  "ratepay.installmentAmount": "ratepay.installmentAmount4",
  "ratepay.interestRate": "ratepay.interestRate8",
  "ratepay.lastInstallmentAmount": "ratepay.lastInstallmentAmount0",
  "ratepay.paymentFirstday": "ratepay.paymentFirstday2",
  "ratepaydata.deliveryDate": "ratepaydata.deliveryDate2"
}
```

