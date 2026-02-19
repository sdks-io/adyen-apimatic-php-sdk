
# Mandate

## Structure

`Mandate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `string` | Required | The billing amount (in minor units) of the recurring transactions. | getAmount(): string | setAmount(string amount): void |
| `amountRule` | [`?string(AmountRule)`](../../doc/models/amount-rule.md) | Optional | The limitation rule of the billing amount.<br><br>Possible values:<br><br>* **max**: The transaction amount can not exceed the `amount`.<br><br>* **exact**: The transaction amount should be the same as the `amount`. | getAmountRule(): ?string | setAmountRule(?string amountRule): void |
| `billingAttemptsRule` | [`?string(BillingAttemptsRule)`](../../doc/models/billing-attempts-rule.md) | Optional | The rule to specify the period, within which the recurring debit can happen, relative to the mandate recurring date.<br><br>Possible values:<br><br>* **on**: On a specific date.<br><br>* **before**:  Before and on a specific date.<br><br>* **after**: On and after a specific date. | getBillingAttemptsRule(): ?string | setBillingAttemptsRule(?string billingAttemptsRule): void |
| `billingDay` | `?string` | Optional | The number of the day, on which the recurring debit can happen. Should be within the same calendar month as the mandate recurring date.<br><br>Possible values: 1-31 based on the `frequency`. | getBillingDay(): ?string | setBillingDay(?string billingDay): void |
| `count` | `?string` | Optional | The number of transactions that can be performed within the given frequency. | getCount(): ?string | setCount(?string count): void |
| `endsAt` | `string` | Required | End date of the billing plan, in YYYY-MM-DD format. | getEndsAt(): string | setEndsAt(string endsAt): void |
| `frequency` | [`string(Frequency)`](../../doc/models/frequency.md) | Required | The frequency with which a shopper should be charged.<br><br>Possible values: **adhoc**, **daily**, **weekly**, **biWeekly**, **monthly**, **quarterly**, **halfYearly**, **yearly**. | getFrequency(): string | setFrequency(string frequency): void |
| `remarks` | `?string` | Optional | The message shown by UPI to the shopper on the approval screen. | getRemarks(): ?string | setRemarks(?string remarks): void |
| `startsAt` | `?string` | Optional | Start date of the billing plan, in YYYY-MM-DD format. By default, the transaction date. | getStartsAt(): ?string | setStartsAt(?string startsAt): void |

## Example (as JSON)

```json
{
  "amount": "amount4",
  "amountRule": "max",
  "billingAttemptsRule": "on",
  "billingDay": "billingDay4",
  "count": "count2",
  "endsAt": "endsAt2",
  "frequency": "halfYearly",
  "remarks": "remarks2"
}
```

