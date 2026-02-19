
# Stored Payment Method Request

## Structure

`StoredPaymentMethodRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantAccount` | `string` | Required | The merchant account identifier, with which you want to process the transaction. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `paymentMethod` | [`PaymentMethodToStore1`](../../doc/models/payment-method-to-store-1.md) | Required | Contains the information required to store a payment method. | getPaymentMethod(): PaymentMethodToStore1 | setPaymentMethod(PaymentMethodToStore1 paymentMethod): void |
| `recurringProcessingModel` | [`string(RecurringProcessingModel1)`](../../doc/models/recurring-processing-model-1.md) | Required | Defines a recurring payment type. Required when creating a token to store payment details.<br>Allowed values:<br><br>* `Subscription` – A transaction for a fixed or variable amount, which follows a fixed schedule.<br>* `CardOnFile` – With a card-on-file (CoF) transaction, card details are stored to enable one-click or omnichannel journeys, or simply to streamline the checkout process. Any subscription not following a fixed schedule is also considered a card-on-file transaction.<br>* `UnscheduledCardOnFile` – An unscheduled card-on-file (UCoF) transaction is a transaction that occurs on a non-fixed schedule and/or have variable amounts. For example, automatic top-ups when a cardholder's balance drops below a certain amount. | getRecurringProcessingModel(): string | setRecurringProcessingModel(string recurringProcessingModel): void |
| `shopperEmail` | `?string` | Optional | The shopper's email address. We recommend that you provide this data, as it is used in velocity fraud checks. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `shopperIp` | `?string` | Optional | The IP address of a shopper. | getShopperIp(): ?string | setShopperIp(?string shopperIp): void |
| `shopperReference` | `string` | Required | A unique identifier for the shopper (for example, user ID or account ID). | getShopperReference(): string | setShopperReference(string shopperReference): void |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount6",
  "paymentMethod": {
    "brand": "brand6",
    "cvc": "cvc6",
    "encryptedCard": "encryptedCard4",
    "encryptedCardNumber": "encryptedCardNumber0",
    "encryptedExpiryMonth": "encryptedExpiryMonth2"
  },
  "recurringProcessingModel": "UnscheduledCardOnFile",
  "shopperEmail": "shopperEmail2",
  "shopperIP": "shopperIP2",
  "shopperReference": "shopperReference2"
}
```

