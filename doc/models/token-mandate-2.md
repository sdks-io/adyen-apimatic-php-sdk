
# Token Mandate 2

Mandate details for the stored payment method.

## Structure

`TokenMandate2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountIdType` | `?string` | Optional | The type of account identifier for the masked account number. | getAccountIdType(): ?string | setAccountIdType(?string accountIdType): void |
| `amount` | `string` | Required | The billing amount (in minor units) of the recurring transactions. | getAmount(): string | setAmount(string amount): void |
| `amountRule` | [`?string(AmountRule)`](../../doc/models/amount-rule.md) | Optional | The limitation rule of the billing amount.<br><br>Possible values:<br><br>* **max**: The transaction amount can not exceed the `amount`.<br><br>* **exact**: The transaction amount should be the same as the `amount`. | getAmountRule(): ?string | setAmountRule(?string amountRule): void |
| `billingAttemptsRule` | [`?string(BillingAttemptsRule)`](../../doc/models/billing-attempts-rule.md) | Optional | The rule to specify the period, within which the recurring debit can happen, relative to the mandate recurring date.<br><br>Possible values:<br><br>* **on**: On a specific date.<br><br>* **before**:  Before and on a specific date.<br><br>* **after**: On and after a specific date. | getBillingAttemptsRule(): ?string | setBillingAttemptsRule(?string billingAttemptsRule): void |
| `billingDay` | `?string` | Optional | The number of the day, on which the recurring debit can happen. Should be within the same calendar month as the mandate recurring date.<br><br>Possible values: 1-31 based on the `frequency`. | getBillingDay(): ?string | setBillingDay(?string billingDay): void |
| `count` | `?string` | Optional | The number of transactions that can be performed within the given frequency. | getCount(): ?string | setCount(?string count): void |
| `currency` | `string` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). | getCurrency(): string | setCurrency(string currency): void |
| `endsAt` | `string` | Required | End date of the billing plan, in YYYY-MM-DD format. | getEndsAt(): string | setEndsAt(string endsAt): void |
| `frequency` | [`string(Frequency)`](../../doc/models/frequency.md) | Required | The frequency with which a shopper should be charged.<br><br>Possible values: **adhoc**, **daily**, **weekly**, **biWeekly**, **monthly**, **quarterly**, **halfYearly**, **yearly**. | getFrequency(): string | setFrequency(string frequency): void |
| `mandateId` | `string` | Required | The unique identifier of the mandate. | getMandateId(): string | setMandateId(string mandateId): void |
| `maskedAccountId` | `?string` | Optional | The masked account number associated with the mandate. | getMaskedAccountId(): ?string | setMaskedAccountId(?string maskedAccountId): void |
| `providerId` | `string` | Required | The provider-specific identifier for this mandate. | getProviderId(): string | setProviderId(string providerId): void |
| `remarks` | `?string` | Optional | Additional remarks or notes about the mandate. | getRemarks(): ?string | setRemarks(?string remarks): void |
| `startsAt` | `?string` | Optional | Start date of the billing plan, in YYYY-MM-DD format. By default, the transaction date. | getStartsAt(): ?string | setStartsAt(?string startsAt): void |
| `status` | `string` | Required | The status of the mandate. Examples : active, revoked, completed, expired | getStatus(): string | setStatus(string status): void |
| `txVariant` | `string` | Required | The transaction variant used for this mandate. | getTxVariant(): string | setTxVariant(string txVariant): void |

## Example (as JSON)

```json
{
  "accountIdType": "accountIdType8",
  "amount": "amount0",
  "amountRule": "max",
  "billingAttemptsRule": "on",
  "billingDay": "billingDay0",
  "count": "count4",
  "currency": "currency8",
  "endsAt": "endsAt8",
  "frequency": "halfYearly",
  "mandateId": "mandateId0",
  "providerId": "providerId2",
  "status": "status0",
  "txVariant": "txVariant6"
}
```

