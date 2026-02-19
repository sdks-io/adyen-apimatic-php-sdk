
# Payment Refund Request

## Structure

`PaymentRefundRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | [`Amount37`](../../doc/models/amount-37.md) | Required | The amount that you want to refund. The `currency` must match the currency used in authorisation, the `value` must be smaller than or equal to the authorised amount. | getAmount(): Amount37 | setAmount(Amount37 amount): void |
| `applicationInfo` | [`?ApplicationInfo1`](../../doc/models/application-info-1.md) | Optional | Information about your application. For more details, see [Building Adyen solutions](https://docs.adyen.com/development-resources/building-adyen-solutions). | getApplicationInfo(): ?ApplicationInfo1 | setApplicationInfo(?ApplicationInfo1 applicationInfo): void |
| `capturePspReference` | `?string` | Optional | This is only available for PayPal refunds. The [`pspReference`](https://docs.adyen.com/api-explorer/Checkout/latest/post/payments#responses-200-pspReference) of the specific capture to refund. | getCapturePspReference(): ?string | setCapturePspReference(?string capturePspReference): void |
| `enhancedSchemeData` | [`?EnhancedSchemeData1`](../../doc/models/enhanced-scheme-data-1.md) | Optional | Enhanced scheme data that may be required for processing the payment. For example, airline information. | getEnhancedSchemeData(): ?EnhancedSchemeData1 | setEnhancedSchemeData(?EnhancedSchemeData1 enhancedSchemeData): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | Price and product information of the refunded items, required for [partial refunds](https://docs.adyen.com/online-payments/refund#refund-a-payment).<br><br>> This field is required for partial refunds with 3x 4x Oney, Affirm, Afterpay, Atome, Clearpay, Klarna, Ratepay, Walley, and Zip. | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `merchantAccount` | `string` | Required | The merchant account that is used to process the payment. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `merchantRefundReason` | [`?string(MerchantRefundReason)`](../../doc/models/merchant-refund-reason.md) | Optional | The reason for the refund request.<br><br>Possible values:<br><br>* **FRAUD**<br><br>* **CUSTOMER REQUEST**<br><br>* **RETURN**<br><br>* **DUPLICATE**<br><br>* **OTHER** | getMerchantRefundReason(): ?string | setMerchantRefundReason(?string merchantRefundReason): void |
| `reference` | `?string` | Optional | Your reference for the refund request. Maximum length: 80 characters. | getReference(): ?string | setReference(?string reference): void |
| `splits` | [`?(Split[])`](../../doc/models/split.md) | Optional | An array of objects specifying how the amount should be split between accounts when using Adyen for Platforms. For more information, see how to process payments for [marketplaces](https://docs.adyen.com/marketplaces/split-payments) or [platforms](https://docs.adyen.com/platforms/online-payments/split-payments/). | getSplits(): ?array | setSplits(?array splits): void |
| `store` | `?string` | Optional | The online store or [physical store](https://docs.adyen.com/point-of-sale/design-your-integration/determine-account-structure/#create-stores) that is processing the refund. This must be the same as the store name configured in your Customer Area.  Otherwise, you get an error and the refund fails. | getStore(): ?string | setStore(?string store): void |

## Example (as JSON)

```json
{
  "amount": {
    "currency": "currency2",
    "value": 110
  },
  "applicationInfo": {
    "adyenLibrary": {
      "name": "name8",
      "version": "version4"
    },
    "adyenPaymentSource": {
      "name": "name2",
      "version": "version8"
    },
    "externalPlatform": {
      "integrator": "integrator0",
      "name": "name4",
      "version": "version0"
    },
    "merchantApplication": {
      "name": "name2",
      "version": "version8"
    },
    "merchantDevice": {
      "os": "os4",
      "osVersion": "osVersion6",
      "reference": "reference8"
    }
  },
  "capturePspReference": "capturePspReference6",
  "enhancedSchemeData": {
    "airline": {
      "agency": {
        "invoiceNumber": "invoiceNumber6",
        "planName": "planName6"
      },
      "boardingFee": 160,
      "code": "code0",
      "computerizedReservationSystem": "computerizedReservationSystem4",
      "customerReferenceNumber": "customerReferenceNumber6",
      "passengerName": "passengerName0"
    },
    "levelTwoThree": {
      "customerReferenceNumber": "customerReferenceNumber0",
      "destination": {
        "countryCode": "countryCode0",
        "postalCode": "postalCode6",
        "stateOrProvince": "stateOrProvince2"
      },
      "dutyAmount": 234,
      "freightAmount": 136,
      "itemDetailLines": [
        {
          "commodityCode": "commodityCode4",
          "description": "description8",
          "discountAmount": 220,
          "productCode": "productCode0",
          "quantity": 184
        }
      ]
    }
  },
  "lineItems": [
    {
      "amountExcludingTax": 38,
      "amountIncludingTax": 148,
      "brand": "brand6",
      "color": "color6",
      "description": "description2"
    },
    {
      "amountExcludingTax": 38,
      "amountIncludingTax": 148,
      "brand": "brand6",
      "color": "color6",
      "description": "description2"
    }
  ],
  "merchantAccount": "merchantAccount0",
  "merchantRefundReason": "DUPLICATE"
}
```

