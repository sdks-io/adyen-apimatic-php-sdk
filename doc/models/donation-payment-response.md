
# Donation Payment Response

## Structure

`DonationPaymentResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`?Amount25`](../../doc/models/amount-25.md) | Optional | Authorised amount in the transaction. | getAmount(): ?Amount25 | setAmount(?Amount25 amount): void |
| `donationAccount` | `?string` | Optional | The Adyen account name of your charity. We will provide you with this account name once your chosen charity has been [onboarded](https://docs.adyen.com/online-payments/donations#onboarding). | getDonationAccount(): ?string | setDonationAccount(?string donationAccount): void |
| `id` | `?string` | Optional | Your unique resource identifier. | getId(): ?string | setId(?string id): void |
| `merchantAccount` | `?string` | Optional | The merchant account identifier, with which you want to process the transaction. | getMerchantAccount(): ?string | setMerchantAccount(?string merchantAccount): void |
| `payment` | [`?PaymentResponse9`](../../doc/models/payment-response-9.md) | Optional | Action to be taken for completing the payment. | getPayment(): ?PaymentResponse9 | setPayment(?PaymentResponse9 payment): void |
| `reference` | `?string` | Optional | The reference to uniquely identify a payment. This reference is used in all communication with you about the payment status. We recommend using a unique value per payment; however, it is not a requirement. If you need to provide multiple references for a transaction, separate them with hyphens ("-"). Maximum length: 80 characters. | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(Status1)`](../../doc/models/status-1.md) | Optional | The status of the donation transaction.<br><br>Possible values:<br><br>* **completed**<br>* **pending**<br>* **refused** | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "donationAccount": "donationAccount4",
  "id": "id0",
  "merchantAccount": "merchantAccount2",
  "payment": {
    "action": {
      "paymentData": "paymentData8",
      "paymentMethodType": "paymentMethodType8",
      "type": "type4",
      "url": "url0"
    },
    "additionalData": {
      "key0": "additionalData6"
    },
    "amount": {
      "currency": "currency2",
      "value": 110
    },
    "donationToken": "donationToken8",
    "fraudResult": {
      "accountScore": 232,
      "results": [
        {
          "accountScore": 102,
          "checkId": 246,
          "name": "name6"
        },
        {
          "accountScore": 102,
          "checkId": 246,
          "name": "name6"
        }
      ]
    }
  }
}
```

