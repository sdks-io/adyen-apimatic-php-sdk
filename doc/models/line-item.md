
# Line Item

## Structure

`LineItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amountExcludingTax` | `?int` | Optional | Item amount excluding the tax, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). | getAmountExcludingTax(): ?int | setAmountExcludingTax(?int amountExcludingTax): void |
| `amountIncludingTax` | `?int` | Optional | Item amount including the tax, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). | getAmountIncludingTax(): ?int | setAmountIncludingTax(?int amountIncludingTax): void |
| `brand` | `?string` | Optional | Brand of the item. | getBrand(): ?string | setBrand(?string brand): void |
| `color` | `?string` | Optional | Color of the item. | getColor(): ?string | setColor(?string color): void |
| `description` | `?string` | Optional | Description of the line item.<br><br>**Constraints**: *Maximum Length*: `10000` | getDescription(): ?string | setDescription(?string description): void |
| `id` | `?string` | Optional | ID of the line item. | getId(): ?string | setId(?string id): void |
| `imageUrl` | `?string` | Optional | Link to the picture of the purchased item. | getImageUrl(): ?string | setImageUrl(?string imageUrl): void |
| `itemCategory` | `?string` | Optional | Item category, used by the payment methods PayPal and Ratepay. | getItemCategory(): ?string | setItemCategory(?string itemCategory): void |
| `manufacturer` | `?string` | Optional | Manufacturer of the item. | getManufacturer(): ?string | setManufacturer(?string manufacturer): void |
| `marketplaceSellerId` | `?string` | Optional | Marketplace seller id. | getMarketplaceSellerId(): ?string | setMarketplaceSellerId(?string marketplaceSellerId): void |
| `productUrl` | `?string` | Optional | Link to the purchased item. | getProductUrl(): ?string | setProductUrl(?string productUrl): void |
| `quantity` | `?int` | Optional | Number of items. | getQuantity(): ?int | setQuantity(?int quantity): void |
| `receiverEmail` | `?string` | Optional | Email associated with the given product in the basket (usually in electronic gift cards). | getReceiverEmail(): ?string | setReceiverEmail(?string receiverEmail): void |
| `size` | `?string` | Optional | Size of the item. | getSize(): ?string | setSize(?string size): void |
| `sku` | `?string` | Optional | Stock keeping unit. | getSku(): ?string | setSku(?string sku): void |
| `taxAmount` | `?int` | Optional | Tax amount, in [minor units](https://docs.adyen.com/development-resources/currency-codes/#minor-units). | getTaxAmount(): ?int | setTaxAmount(?int taxAmount): void |
| `taxPercentage` | `?int` | Optional | Tax percentage, represented as a [basis point](https://en.wikipedia.org/wiki/Basis_point) integer. For example:<br><br>- **530** for 5.3% (five point three percent)<br>- **2100** for 21% (twenty-one percent) | getTaxPercentage(): ?int | setTaxPercentage(?int taxPercentage): void |
| `upc` | `?string` | Optional | Universal Product Code. | getUpc(): ?string | setUpc(?string upc): void |

## Example (as JSON)

```json
{
  "amountExcludingTax": 36,
  "amountIncludingTax": 146,
  "brand": "brand0",
  "color": "color0",
  "description": "description6"
}
```

