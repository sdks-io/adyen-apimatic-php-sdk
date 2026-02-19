
# Configuration

## Structure

`Configuration`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brand` | `string` | Required | Payment method, like **eftpos_australia** or **mc**. See the [possible values](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api). | getBrand(): string | setBrand(string brand): void |
| `commercial` | `?bool` | Optional | Set to **true** to apply surcharges only to commercial/business cards. | getCommercial(): ?bool | setCommercial(?bool commercial): void |
| `country` | `?(string[])` | Optional | The country/region of the card issuer. If used, the surcharge settings only apply to the card issued in that country/region. | getCountry(): ?array | setCountry(?array country): void |
| `currencies` | [`Currency[]`](../../doc/models/currency.md) | Required | Currency and percentage or amount of the surcharge. | getCurrencies(): array | setCurrencies(array currencies): void |
| `sources` | `?(string[])` | Optional | Funding source. Possible values:<br><br>* **Credit**<br>* **Debit** | getSources(): ?array | setSources(?array sources): void |

## Example (as JSON)

```json
{
  "brand": "brand6",
  "currencies": [
    {
      "amount": 208,
      "currencyCode": "currencyCode6",
      "maxAmount": 98,
      "percentage": 191.04
    }
  ],
  "commercial": false,
  "country": [
    "country3",
    "country4",
    "country5"
  ],
  "sources": [
    "sources4"
  ]
}
```

