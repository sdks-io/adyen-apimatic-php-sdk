
# Card Details Response

## Structure

`CardDetailsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brands` | [`?(CardBrandDetails[])`](../../doc/models/card-brand-details.md) | Optional | The list of brands identified for the card. | getBrands(): ?array | setBrands(?array brands): void |
| `fundingSource` | `?string` | Optional | The funding source of the card, for example **DEBIT**, **CREDIT**, or **PREPAID**. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `isCardCommercial` | `?bool` | Optional | Indicates if this is a commercial card or a consumer card. If **true**, it is a commercial card. If **false**, it is a consumer card. | getIsCardCommercial(): ?bool | setIsCardCommercial(?bool isCardCommercial): void |
| `issuingCountryCode` | `?string` | Optional | The two-letter country code  of the country where the card was issued. | getIssuingCountryCode(): ?string | setIssuingCountryCode(?string issuingCountryCode): void |

## Example (as JSON)

```json
{
  "brands": [
    {
      "supported": false,
      "type": "type6"
    },
    {
      "supported": false,
      "type": "type6"
    },
    {
      "supported": false,
      "type": "type6"
    }
  ],
  "fundingSource": "fundingSource4",
  "isCardCommercial": false,
  "issuingCountryCode": "issuingCountryCode4"
}
```

