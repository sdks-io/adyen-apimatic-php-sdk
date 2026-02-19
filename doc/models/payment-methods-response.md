
# Payment Methods Response

## Structure

`PaymentMethodsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `paymentMethods` | [`?(PaymentMethod[])`](../../doc/models/payment-method.md) | Optional | Detailed list of payment methods required to generate payment forms. | getPaymentMethods(): ?array | setPaymentMethods(?array paymentMethods): void |
| `storedPaymentMethods` | [`?(StoredPaymentMethod2[])`](../../doc/models/stored-payment-method-2.md) | Optional | List of all stored payment methods. | getStoredPaymentMethods(): ?array | setStoredPaymentMethods(?array storedPaymentMethods): void |

## Example (as JSON)

```json
{
  "paymentMethods": [
    {
      "apps": [
        {
          "id": "id6",
          "name": "name6"
        },
        {
          "id": "id6",
          "name": "name6"
        }
      ],
      "brand": "brand6",
      "brands": [
        "brands3"
      ],
      "configuration": {
        "key0": "configuration2",
        "key1": "configuration1",
        "key2": "configuration0"
      },
      "fundingSource": "debit"
    }
  ],
  "storedPaymentMethods": [
    {
      "bankAccountNumber": "bankAccountNumber2",
      "bankLocationId": "bankLocationId6",
      "brand": "brand6",
      "expiryMonth": "expiryMonth6",
      "expiryYear": "expiryYear6"
    },
    {
      "bankAccountNumber": "bankAccountNumber2",
      "bankLocationId": "bankLocationId6",
      "brand": "brand6",
      "expiryMonth": "expiryMonth6",
      "expiryYear": "expiryYear6"
    },
    {
      "bankAccountNumber": "bankAccountNumber2",
      "bankLocationId": "bankLocationId6",
      "brand": "brand6",
      "expiryMonth": "expiryMonth6",
      "expiryYear": "expiryYear6"
    }
  ]
}
```

