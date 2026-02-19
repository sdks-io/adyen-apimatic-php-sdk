
# Additional Data Open Invoice

## Structure

`AdditionalDataOpenInvoice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `openinvoicedataMerchantData` | `?string` | Optional | Holds different merchant data points like product, purchase, customer, and so on. It takes data in a Base64 encoded string.<br><br>The `merchantData` parameter needs to be added to the `openinvoicedata` signature at the end.<br><br>Since the field is optional, if it's not included it does not impact computing the merchant signature.<br><br>Applies only to Klarna.<br><br>You can contact Klarna for the format and structure of the string. | getOpeninvoicedataMerchantData(): ?string | setOpeninvoicedataMerchantData(?string openinvoicedataMerchantData): void |
| `openinvoicedataNumberOfLines` | `?string` | Optional | The number of invoice lines included in `openinvoicedata`.<br><br>There needs to be at least one line, so `numberOfLines` needs to be at least 1. | getOpeninvoicedataNumberOfLines(): ?string | setOpeninvoicedataNumberOfLines(?string openinvoicedataNumberOfLines): void |
| `openinvoicedataRecipientFirstName` | `?string` | Optional | First name of the recipient. If the delivery address and the billing address are different, specify the `recipientFirstName` and `recipientLastName` to share the delivery address with Klarna. Otherwise, only the billing address is shared with Klarna. | getOpeninvoicedataRecipientFirstName(): ?string | setOpeninvoicedataRecipientFirstName(?string openinvoicedataRecipientFirstName): void |
| `openinvoicedataRecipientLastName` | `?string` | Optional | Last name of the recipient. If the delivery address and the billing address are different, specify the `recipientFirstName` and `recipientLastName` to share the delivery address with Klarna. Otherwise, only the billing address is shared with Klarna. | getOpeninvoicedataRecipientLastName(): ?string | setOpeninvoicedataRecipientLastName(?string openinvoicedataRecipientLastName): void |
| `openinvoicedataLineItemNrCurrencyCode` | `?string` | Optional | The three-character ISO currency code. | getOpeninvoicedataLineItemNrCurrencyCode(): ?string | setOpeninvoicedataLineItemNrCurrencyCode(?string openinvoicedataLineItemNrCurrencyCode): void |
| `openinvoicedataLineItemNrDescription` | `?string` | Optional | A text description of the product the invoice line refers to. | getOpeninvoicedataLineItemNrDescription(): ?string | setOpeninvoicedataLineItemNrDescription(?string openinvoicedataLineItemNrDescription): void |
| `openinvoicedataLineItemNrItemAmount` | `?string` | Optional | The price for one item in the invoice line, represented in minor units.<br><br>The due amount for the item, VAT excluded. | getOpeninvoicedataLineItemNrItemAmount(): ?string | setOpeninvoicedataLineItemNrItemAmount(?string openinvoicedataLineItemNrItemAmount): void |
| `openinvoicedataLineItemNrItemId` | `?string` | Optional | A unique id for this item. Required for RatePay if the description of each item is not unique. | getOpeninvoicedataLineItemNrItemId(): ?string | setOpeninvoicedataLineItemNrItemId(?string openinvoicedataLineItemNrItemId): void |
| `openinvoicedataLineItemNrItemVatAmount` | `?string` | Optional | The VAT due for one item in the invoice line, represented in minor units. | getOpeninvoicedataLineItemNrItemVatAmount(): ?string | setOpeninvoicedataLineItemNrItemVatAmount(?string openinvoicedataLineItemNrItemVatAmount): void |
| `openinvoicedataLineItemNrItemVatPercentage` | `?string` | Optional | The VAT percentage for one item in the invoice line, represented in minor units.<br><br>For example, 19% VAT is specified as 1900. | getOpeninvoicedataLineItemNrItemVatPercentage(): ?string | setOpeninvoicedataLineItemNrItemVatPercentage(?string openinvoicedataLineItemNrItemVatPercentage): void |
| `openinvoicedataLineItemNrNumberOfItems` | `?string` | Optional | The number of units purchased of a specific product. | getOpeninvoicedataLineItemNrNumberOfItems(): ?string | setOpeninvoicedataLineItemNrNumberOfItems(?string openinvoicedataLineItemNrNumberOfItems): void |
| `openinvoicedataLineItemNrReturnShippingCompany` | `?string` | Optional | Name of the shipping company handling the the return shipment. | getOpeninvoicedataLineItemNrReturnShippingCompany(): ?string | setOpeninvoicedataLineItemNrReturnShippingCompany(?string openinvoicedataLineItemNrReturnShippingCompany): void |
| `openinvoicedataLineItemNrReturnTrackingNumber` | `?string` | Optional | The tracking number for the return of the shipment. | getOpeninvoicedataLineItemNrReturnTrackingNumber(): ?string | setOpeninvoicedataLineItemNrReturnTrackingNumber(?string openinvoicedataLineItemNrReturnTrackingNumber): void |
| `openinvoicedataLineItemNrReturnTrackingUri` | `?string` | Optional | URI where the customer can track the return of their shipment. | getOpeninvoicedataLineItemNrReturnTrackingUri(): ?string | setOpeninvoicedataLineItemNrReturnTrackingUri(?string openinvoicedataLineItemNrReturnTrackingUri): void |
| `openinvoicedataLineItemNrShippingCompany` | `?string` | Optional | Name of the shipping company handling the delivery. | getOpeninvoicedataLineItemNrShippingCompany(): ?string | setOpeninvoicedataLineItemNrShippingCompany(?string openinvoicedataLineItemNrShippingCompany): void |
| `openinvoicedataLineItemNrShippingMethod` | `?string` | Optional | Shipping method. | getOpeninvoicedataLineItemNrShippingMethod(): ?string | setOpeninvoicedataLineItemNrShippingMethod(?string openinvoicedataLineItemNrShippingMethod): void |
| `openinvoicedataLineItemNrTrackingNumber` | `?string` | Optional | The tracking number for the shipment. | getOpeninvoicedataLineItemNrTrackingNumber(): ?string | setOpeninvoicedataLineItemNrTrackingNumber(?string openinvoicedataLineItemNrTrackingNumber): void |
| `openinvoicedataLineItemNrTrackingUri` | `?string` | Optional | URI where the customer can track their shipment. | getOpeninvoicedataLineItemNrTrackingUri(): ?string | setOpeninvoicedataLineItemNrTrackingUri(?string openinvoicedataLineItemNrTrackingUri): void |

## Example (as JSON)

```json
{
  "openinvoicedata.merchantData": "openinvoicedata.merchantData6",
  "openinvoicedata.numberOfLines": "openinvoicedata.numberOfLines8",
  "openinvoicedata.recipientFirstName": "openinvoicedata.recipientFirstName6",
  "openinvoicedata.recipientLastName": "openinvoicedata.recipientLastName6",
  "openinvoicedataLine[itemNr].currencyCode": "openinvoicedataLine[itemNr].currencyCode6"
}
```

