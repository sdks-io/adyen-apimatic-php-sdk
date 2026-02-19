
# Custom Notification 1

Custom test notification object. Required when the [`types`](https://docs.adyen.com/api-explorer/#/ManagementService/v1/post/companies/{companyId}/webhooks/{webhookId}/test__reqParam_types) list contains **CUSTOM**.

## Structure

`CustomNotification1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`?Amount`](../../doc/models/amount.md) | Optional | The amount of the payment that the notification is about. Set the value in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getAmount(): ?Amount | setAmount(?Amount amount): void |
| `eventCode` | `?string` | Optional | The event that caused the notification to be sent.Currently supported values:<br><br>* **AUTHORISATION**<br>* **CANCELLATION**<br>* **REFUND**<br>* **CAPTURE**<br>* **REPORT_AVAILABLE**<br>* **CHARGEBACK**<br>* **REQUEST_FOR_INFORMATION**<br>* **NOTIFICATION_OF_CHARGEBACK**<br>* **NOTIFICATIONTEST**<br>* **ORDER_OPENED**<br>* **ORDER_CLOSED**<br>* **CHARGEBACK_REVERSED**<br>* **REFUNDED_REVERSED**<br>* **REFUND_WITH_DATA** | getEventCode(): ?string | setEventCode(?string eventCode): void |
| `eventDate` | `?DateTime` | Optional | The time of the event. Format: [ISO 8601](http://www.w3.org/TR/NOTE-datetime), YYYY-MM-DDThh:mm:ssTZD. | getEventDate(): ?\DateTime | setEventDate(?\DateTime eventDate): void |
| `merchantReference` | `?string` | Optional | Your reference for the custom test notification. | getMerchantReference(): ?string | setMerchantReference(?string merchantReference): void |
| `paymentMethod` | `?string` | Optional | The payment method for the payment that the notification is about. Possible values:<br><br>* **amex**<br>* **visa**<br>* **mc**<br>* **maestro**<br>* **bcmc**<br>* **paypal**<br>* **sms**<br>* **bankTransfer_NL**<br>* **bankTransfer_DE**<br>* **bankTransfer_BE**<br>* **ideal**<br>* **elv**<br>* **sepadirectdebit** | getPaymentMethod(): ?string | setPaymentMethod(?string paymentMethod): void |
| `reason` | `?string` | Optional | A description of what caused the notification. | getReason(): ?string | setReason(?string reason): void |
| `success` | `?bool` | Optional | The outcome of the event which the notification is about. Set to either **true** or **false**. | getSuccess(): ?bool | setSuccess(?bool success): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "eventCode": "eventCode2",
  "eventDate": "2016-03-13T12:52:32.123Z",
  "merchantReference": "merchantReference4",
  "paymentMethod": "paymentMethod0"
}
```

