
# Paypal Update Order Request

## Structure

`PaypalUpdateOrderRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`?Amount43`](../../doc/models/amount-43.md) | Optional | The updated final payment amount. This amount is the item total plus the shipping costs of the selected `deliveryMethod`. | getAmount(): ?Amount43 | setAmount(?Amount43 amount): void |
| `deliveryMethods` | [`?(DeliveryMethod[])`](../../doc/models/delivery-method.md) | Optional | The list of new delivery methods and the cost of each. | getDeliveryMethods(): ?array | setDeliveryMethods(?array deliveryMethods): void |
| `paymentData` | `?string` | Optional | The `paymentData` from the client side. This value changes every time you make a `/paypal/updateOrder` request. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `pspReference` | `?string` | Optional | The original `pspReference` from the `/payments` response. | getPspReference(): ?string | setPspReference(?string pspReference): void |
| `sessionId` | `?string` | Optional | The original `sessionId` from the `/sessions` response. | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `taxTotal` | [`?TaxTotal2`](../../doc/models/tax-total-2.md) | Optional | Total tax amount from the order. | getTaxTotal(): ?TaxTotal2 | setTaxTotal(?TaxTotal2 taxTotal): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "deliveryMethods": [
    {
      "amount": {
        "currency": "currency2",
        "value": 110
      },
      "description": "description6",
      "reference": "reference2",
      "selected": false,
      "type": "Shipping"
    }
  ],
  "paymentData": "paymentData0",
  "pspReference": "pspReference0",
  "sessionId": "sessionId6"
}
```

