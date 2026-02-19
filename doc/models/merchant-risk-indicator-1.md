
# Merchant Risk Indicator 1

Additional risk fields for 3D Secure 2.

> For 3D Secure 2 transactions, we recommend that you include this object to increase the chances of achieving a frictionless flow.

## Structure

`MerchantRiskIndicator1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addressMatch` | `?bool` | Optional | Whether the chosen delivery address is identical to the billing address. | getAddressMatch(): ?bool | setAddressMatch(?bool addressMatch): void |
| `deliveryAddressIndicator` | [`?string(DeliveryAddressIndicator)`](../../doc/models/delivery-address-indicator.md) | Optional | Indicator regarding the delivery address.<br>Allowed values:<br><br>* `shipToBillingAddress`<br>* `shipToVerifiedAddress`<br>* `shipToNewAddress`<br>* `shipToStore`<br>* `digitalGoods`<br>* `goodsNotShipped`<br>* `other` | getDeliveryAddressIndicator(): ?string | setDeliveryAddressIndicator(?string deliveryAddressIndicator): void |
| `deliveryEmail` | `?string` | Optional | The delivery email address (for digital goods). | getDeliveryEmail(): ?string | setDeliveryEmail(?string deliveryEmail): void |
| `deliveryEmailAddress` | `?string` | Optional | For Electronic delivery, the email address to which the merchandise was delivered. Maximum length: 254 characters.<br><br>**Constraints**: *Maximum Length*: `254` | getDeliveryEmailAddress(): ?string | setDeliveryEmailAddress(?string deliveryEmailAddress): void |
| `deliveryTimeframe` | [`?string(DeliveryTimeframe)`](../../doc/models/delivery-timeframe.md) | Optional | The estimated delivery time for the shopper to receive the goods.<br>Allowed values:<br><br>* `electronicDelivery`<br>* `sameDayShipping`<br>* `overnightShipping`<br>* `twoOrMoreDaysShipping` | getDeliveryTimeframe(): ?string | setDeliveryTimeframe(?string deliveryTimeframe): void |
| `giftCardAmount` | [`?Amount7`](../../doc/models/amount-7.md) | Optional | For prepaid or gift card purchase, the purchase amount total of prepaid or gift card(s). | getGiftCardAmount(): ?Amount7 | setGiftCardAmount(?Amount7 giftCardAmount): void |
| `giftCardCount` | `?int` | Optional | For prepaid or gift card purchase, total count of individual prepaid or gift cards/codes purchased. | getGiftCardCount(): ?int | setGiftCardCount(?int giftCardCount): void |
| `giftCardCurr` | `?string` | Optional | For prepaid or gift card purchase, [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) three-digit currency code of the gift card, other than those listed in Table A.5 of the EMVCo 3D Secure Protocol and Core Functions Specification. | getGiftCardCurr(): ?string | setGiftCardCurr(?string giftCardCurr): void |
| `preOrderDate` | `?DateTime` | Optional | For pre-order purchases, the expected date this product will be available to the shopper. | getPreOrderDate(): ?\DateTime | setPreOrderDate(?\DateTime preOrderDate): void |
| `preOrderPurchase` | `?bool` | Optional | Indicator for whether this transaction is for pre-ordering a product. | getPreOrderPurchase(): ?bool | setPreOrderPurchase(?bool preOrderPurchase): void |
| `preOrderPurchaseInd` | `?string` | Optional | Indicates whether Cardholder is placing an order for merchandise with a future availability or release date. | getPreOrderPurchaseInd(): ?string | setPreOrderPurchaseInd(?string preOrderPurchaseInd): void |
| `reorderItems` | `?bool` | Optional | Indicator for whether the shopper has already purchased the same items in the past. | getReorderItems(): ?bool | setReorderItems(?bool reorderItems): void |
| `reorderItemsInd` | `?string` | Optional | Indicates whether the cardholder is reordering previously purchased merchandise. | getReorderItemsInd(): ?string | setReorderItemsInd(?string reorderItemsInd): void |
| `shipIndicator` | `?string` | Optional | Indicates shipping method chosen for the transaction. | getShipIndicator(): ?string | setShipIndicator(?string shipIndicator): void |

## Example (as JSON)

```json
{
  "addressMatch": false,
  "deliveryAddressIndicator": "shipToBillingAddress",
  "deliveryEmail": "deliveryEmail8",
  "deliveryEmailAddress": "deliveryEmailAddress8",
  "deliveryTimeframe": "overnightShipping"
}
```

