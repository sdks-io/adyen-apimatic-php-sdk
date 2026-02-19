
# Account Info 1

Shopper account information for 3D Secure 2.

> For 3D Secure 2 transactions, we recommend that you include this object to increase the chances of achieving a frictionless flow.

## Structure

`AccountInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountAgeIndicator` | [`?string(AccountAgeIndicator)`](../../doc/models/account-age-indicator.md) | Optional | Indicator for the length of time since this shopper account was created in the merchant's environment.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days | getAccountAgeIndicator(): ?string | setAccountAgeIndicator(?string accountAgeIndicator): void |
| `accountChangeDate` | `?DateTime` | Optional | Date when the shopper's account was last changed. | getAccountChangeDate(): ?\DateTime | setAccountChangeDate(?\DateTime accountChangeDate): void |
| `accountChangeIndicator` | [`?string(AccountChangeIndicator)`](../../doc/models/account-change-indicator.md) | Optional | Indicator for the length of time since the shopper's account was last updated.<br>Allowed values:<br><br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days | getAccountChangeIndicator(): ?string | setAccountChangeIndicator(?string accountChangeIndicator): void |
| `accountCreationDate` | `?DateTime` | Optional | Date when the shopper's account was created. | getAccountCreationDate(): ?\DateTime | setAccountCreationDate(?\DateTime accountCreationDate): void |
| `accountType` | [`?string(AccountType)`](../../doc/models/account-type.md) | Optional | Indicates the type of account. For example, for a multi-account card product.<br>Allowed values:<br><br>* notApplicable<br>* credit<br>* debit | getAccountType(): ?string | setAccountType(?string accountType): void |
| `addCardAttemptsDay` | `?int` | Optional | Number of attempts the shopper tried to add a card to their account in the last day. | getAddCardAttemptsDay(): ?int | setAddCardAttemptsDay(?int addCardAttemptsDay): void |
| `deliveryAddressUsageDate` | `?DateTime` | Optional | Date the selected delivery address was first used. | getDeliveryAddressUsageDate(): ?\DateTime | setDeliveryAddressUsageDate(?\DateTime deliveryAddressUsageDate): void |
| `deliveryAddressUsageIndicator` | [`?string(DeliveryAddressUsageIndicator)`](../../doc/models/delivery-address-usage-indicator.md) | Optional | Indicator for the length of time since this delivery address was first used.<br>Allowed values:<br><br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days | getDeliveryAddressUsageIndicator(): ?string | setDeliveryAddressUsageIndicator(?string deliveryAddressUsageIndicator): void |
| `homePhone` | `?string` | Optional | Shopper's home phone number (including the country code). | getHomePhone(): ?string | setHomePhone(?string homePhone): void |
| `mobilePhone` | `?string` | Optional | Shopper's mobile phone number (including the country code). | getMobilePhone(): ?string | setMobilePhone(?string mobilePhone): void |
| `passwordChangeDate` | `?DateTime` | Optional | Date when the shopper last changed their password. | getPasswordChangeDate(): ?\DateTime | setPasswordChangeDate(?\DateTime passwordChangeDate): void |
| `passwordChangeIndicator` | [`?string(PasswordChangeIndicator)`](../../doc/models/password-change-indicator.md) | Optional | Indicator when the shopper has changed their password.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days | getPasswordChangeIndicator(): ?string | setPasswordChangeIndicator(?string passwordChangeIndicator): void |
| `pastTransactionsDay` | `?int` | Optional | Number of all transactions (successful and abandoned) from this shopper in the past 24 hours. | getPastTransactionsDay(): ?int | setPastTransactionsDay(?int pastTransactionsDay): void |
| `pastTransactionsYear` | `?int` | Optional | Number of all transactions (successful and abandoned) from this shopper in the past year. | getPastTransactionsYear(): ?int | setPastTransactionsYear(?int pastTransactionsYear): void |
| `paymentAccountAge` | `?DateTime` | Optional | Date this payment method was added to the shopper's account. | getPaymentAccountAge(): ?\DateTime | setPaymentAccountAge(?\DateTime paymentAccountAge): void |
| `paymentAccountIndicator` | [`?string(PaymentAccountIndicator)`](../../doc/models/payment-account-indicator.md) | Optional | Indicator for the length of time since this payment method was added to this shopper's account.<br>Allowed values:<br><br>* notApplicable<br>* thisTransaction<br>* lessThan30Days<br>* from30To60Days<br>* moreThan60Days | getPaymentAccountIndicator(): ?string | setPaymentAccountIndicator(?string paymentAccountIndicator): void |
| `purchasesLast6Months` | `?int` | Optional | Number of successful purchases in the last six months. | getPurchasesLast6Months(): ?int | setPurchasesLast6Months(?int purchasesLast6Months): void |
| `suspiciousActivity` | `?bool` | Optional | Whether suspicious activity was recorded on this account. | getSuspiciousActivity(): ?bool | setSuspiciousActivity(?bool suspiciousActivity): void |
| `workPhone` | `?string` | Optional | Shopper's work phone number (including the country code). | getWorkPhone(): ?string | setWorkPhone(?string workPhone): void |

## Example (as JSON)

```json
{
  "accountAgeIndicator": "lessThan30Days",
  "accountChangeDate": "2016-03-13T12:52:32.123Z",
  "accountChangeIndicator": "thisTransaction",
  "accountCreationDate": "2016-03-13T12:52:32.123Z",
  "accountType": "debit"
}
```

