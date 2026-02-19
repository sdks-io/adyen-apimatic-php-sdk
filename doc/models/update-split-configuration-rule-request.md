
# Update Split Configuration Rule Request

## Structure

`UpdateSplitConfigurationRuleRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | The currency condition that defines whether the split logic applies.<br>Its value must be a three-character [ISO currency code](https://en.wikipedia.org/wiki/ISO_4217). | getCurrency(): string | setCurrency(string currency): void |
| `fundingSource` | `string` | Required | The funding source of the payment method.<br><br>Possible values:<br><br>* **credit**<br>* **debit**<br>* **prepaid**<br>* **deferred_debit**<br>* **charged**<br>* **ANY** | getFundingSource(): string | setFundingSource(string fundingSource): void |
| `paymentMethod` | `string` | Required | The payment method condition that defines whether the split logic applies.<br><br>Possible values:<br><br>* [Payment method variant](https://docs.adyen.com/development-resources/paymentmethodvariant): Apply the split logic for a specific payment method.<br>* **ANY**: Apply the split logic for all available payment methods. | getPaymentMethod(): string | setPaymentMethod(string paymentMethod): void |
| `shopperInteraction` | `string` | Required | The sales channel condition that defines whether the split logic applies.<br><br>Possible values:<br><br>* **Ecommerce**: Online transactions where the cardholder is present.<br>* **ContAuth**: Card on file and/or subscription transactions, where the cardholder is known to the merchant (returning customer).<br>* **Moto**: Mail-order and telephone-order transactions where the customer is in contact with the merchant via email or telephone.<br>* **POS**: Point-of-sale transactions where the customer is physically present to make a payment using a secure payment terminal.<br>* **ANY**: All sales channels. | getShopperInteraction(): string | setShopperInteraction(string shopperInteraction): void |

## Example (as JSON)

```json
{
  "currency": "currency8",
  "fundingSource": "fundingSource4",
  "paymentMethod": "paymentMethod0",
  "shopperInteraction": "shopperInteraction8"
}
```

