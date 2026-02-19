
# Additional Data Risk

## Structure

`AdditionalDataRisk`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `riskdataCustomFieldName` | `?string` | Optional | The data for your custom risk field. For more information, refer to [Create custom risk fields](https://docs.adyen.com/risk-management/configure-custom-risk-rules#step-1-create-custom-risk-fields). | getRiskdataCustomFieldName(): ?string | setRiskdataCustomFieldName(?string riskdataCustomFieldName): void |
| `riskdataBasketItemItemNrAmountPerItem` | `?string` | Optional | The price of item in the basket, represented in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getRiskdataBasketItemItemNrAmountPerItem(): ?string | setRiskdataBasketItemItemNrAmountPerItem(?string riskdataBasketItemItemNrAmountPerItem): void |
| `riskdataBasketItemItemNrBrand` | `?string` | Optional | Brand of the item. | getRiskdataBasketItemItemNrBrand(): ?string | setRiskdataBasketItemItemNrBrand(?string riskdataBasketItemItemNrBrand): void |
| `riskdataBasketItemItemNrCategory` | `?string` | Optional | Category of the item. | getRiskdataBasketItemItemNrCategory(): ?string | setRiskdataBasketItemItemNrCategory(?string riskdataBasketItemItemNrCategory): void |
| `riskdataBasketItemItemNrColor` | `?string` | Optional | Color of the item. | getRiskdataBasketItemItemNrColor(): ?string | setRiskdataBasketItemItemNrColor(?string riskdataBasketItemItemNrColor): void |
| `riskdataBasketItemItemNrCurrency` | `?string` | Optional | The three-character [ISO currency code](https://en.wikipedia.org/wiki/ISO_4217). | getRiskdataBasketItemItemNrCurrency(): ?string | setRiskdataBasketItemItemNrCurrency(?string riskdataBasketItemItemNrCurrency): void |
| `riskdataBasketItemItemNrItemId` | `?string` | Optional | ID of the item. | getRiskdataBasketItemItemNrItemId(): ?string | setRiskdataBasketItemItemNrItemId(?string riskdataBasketItemItemNrItemId): void |
| `riskdataBasketItemItemNrManufacturer` | `?string` | Optional | Manufacturer of the item. | getRiskdataBasketItemItemNrManufacturer(): ?string | setRiskdataBasketItemItemNrManufacturer(?string riskdataBasketItemItemNrManufacturer): void |
| `riskdataBasketItemItemNrProductTitle` | `?string` | Optional | A text description of the product the invoice line refers to. | getRiskdataBasketItemItemNrProductTitle(): ?string | setRiskdataBasketItemItemNrProductTitle(?string riskdataBasketItemItemNrProductTitle): void |
| `riskdataBasketItemItemNrQuantity` | `?string` | Optional | Quantity of the item purchased. | getRiskdataBasketItemItemNrQuantity(): ?string | setRiskdataBasketItemItemNrQuantity(?string riskdataBasketItemItemNrQuantity): void |
| `riskdataBasketItemItemNrReceiverEmail` | `?string` | Optional | Email associated with the given product in the basket (usually in electronic gift cards). | getRiskdataBasketItemItemNrReceiverEmail(): ?string | setRiskdataBasketItemItemNrReceiverEmail(?string riskdataBasketItemItemNrReceiverEmail): void |
| `riskdataBasketItemItemNrSize` | `?string` | Optional | Size of the item. | getRiskdataBasketItemItemNrSize(): ?string | setRiskdataBasketItemItemNrSize(?string riskdataBasketItemItemNrSize): void |
| `riskdataBasketItemItemNrSku` | `?string` | Optional | [Stock keeping unit](https://en.wikipedia.org/wiki/Stock_keeping_unit). | getRiskdataBasketItemItemNrSku(): ?string | setRiskdataBasketItemItemNrSku(?string riskdataBasketItemItemNrSku): void |
| `riskdataBasketItemItemNrUpc` | `?string` | Optional | [Universal Product Code](https://en.wikipedia.org/wiki/Universal_Product_Code). | getRiskdataBasketItemItemNrUpc(): ?string | setRiskdataBasketItemItemNrUpc(?string riskdataBasketItemItemNrUpc): void |
| `riskdataPromotionsPromotionItemNrPromotionCode` | `?string` | Optional | Code of the promotion. | getRiskdataPromotionsPromotionItemNrPromotionCode(): ?string | setRiskdataPromotionsPromotionItemNrPromotionCode(?string riskdataPromotionsPromotionItemNrPromotionCode): void |
| `riskdataPromotionsPromotionItemNrPromotionDiscountAmount` | `?string` | Optional | The discount amount of the promotion, represented in [minor units](https://docs.adyen.com/development-resources/currency-codes). | getRiskdataPromotionsPromotionItemNrPromotionDiscountAmount(): ?string | setRiskdataPromotionsPromotionItemNrPromotionDiscountAmount(?string riskdataPromotionsPromotionItemNrPromotionDiscountAmount): void |
| `riskdataPromotionsPromotionItemNrPromotionDiscountCurrency` | `?string` | Optional | The three-character [ISO currency code](https://en.wikipedia.org/wiki/ISO_4217). | getRiskdataPromotionsPromotionItemNrPromotionDiscountCurrency(): ?string | setRiskdataPromotionsPromotionItemNrPromotionDiscountCurrency(?string riskdataPromotionsPromotionItemNrPromotionDiscountCurrency): void |
| `riskdataPromotionsPromotionItemNrPromotionDiscountPercentage` | `?string` | Optional | Promotion's percentage discount. It is represented in percentage value and there is no need to include the '%' sign.<br><br>e.g. for a promotion discount of 30%, the value of the field should be 30. | getRiskdataPromotionsPromotionItemNrPromotionDiscountPercentage(): ?string | setRiskdataPromotionsPromotionItemNrPromotionDiscountPercentage(?string riskdataPromotionsPromotionItemNrPromotionDiscountPercentage): void |
| `riskdataPromotionsPromotionItemNrPromotionName` | `?string` | Optional | Name of the promotion. | getRiskdataPromotionsPromotionItemNrPromotionName(): ?string | setRiskdataPromotionsPromotionItemNrPromotionName(?string riskdataPromotionsPromotionItemNrPromotionName): void |
| `riskdataRiskProfileReference` | `?string` | Optional | Reference number of the risk profile that you want to apply to the payment. If not provided or left blank, the merchant-level account's default risk profile will be applied to the payment. For more information, see [dynamically assign a risk profile to a payment](https://docs.adyen.com/risk-management/create-and-use-risk-profiles#dynamically-assign-a-risk-profile-to-a-payment). | getRiskdataRiskProfileReference(): ?string | setRiskdataRiskProfileReference(?string riskdataRiskProfileReference): void |
| `riskdataSkipRisk` | `?string` | Optional | If this parameter is provided with the value **true**, risk checks for the payment request are skipped and the transaction will not get a risk score. | getRiskdataSkipRisk(): ?string | setRiskdataSkipRisk(?string riskdataSkipRisk): void |

## Example (as JSON)

```json
{
  "riskdata.[customFieldName]": "riskdata.[customFieldName]8",
  "riskdata.basket.item[itemNr].amountPerItem": "riskdata.basket.item[itemNr].amountPerItem6",
  "riskdata.basket.item[itemNr].brand": "riskdata.basket.item[itemNr].brand0",
  "riskdata.basket.item[itemNr].category": "riskdata.basket.item[itemNr].category8",
  "riskdata.basket.item[itemNr].color": "riskdata.basket.item[itemNr].color6"
}
```

