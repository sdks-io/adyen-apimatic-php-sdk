
# Payment Method

## Structure

`PaymentMethod`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apps` | [`?(PaymentMethodUpiApps[])`](../../doc/models/payment-method-upi-apps.md) | Optional | A list of apps for this payment method. | getApps(): ?array | setApps(?array apps): void |
| `brand` | `?string` | Optional | Brand for the selected gift card. For example: plastix, hmclub. | getBrand(): ?string | setBrand(?string brand): void |
| `brands` | `?(string[])` | Optional | List of possible brands. For example: visa, mc. | getBrands(): ?array | setBrands(?array brands): void |
| `configuration` | `?array<string,string>` | Optional | The configuration of the payment method. | getConfiguration(): ?array | setConfiguration(?array configuration): void |
| `fundingSource` | [`?string(FundingSource9)`](../../doc/models/funding-source-9.md) | Optional | The funding source of the payment method. | getFundingSource(): ?string | setFundingSource(?string fundingSource): void |
| `group` | [`?PaymentMethodGroup2`](../../doc/models/payment-method-group-2.md) | Optional | The group where this payment method belongs to. | getGroup(): ?PaymentMethodGroup2 | setGroup(?PaymentMethodGroup2 group): void |
| `inputDetails` | [`?(InputDetail[])`](../../doc/models/input-detail.md) | Optional | All input details to be provided to complete the payment with this payment method. | getInputDetails(): ?array | setInputDetails(?array inputDetails): void |
| `issuers` | [`?(PaymentMethodIssuer[])`](../../doc/models/payment-method-issuer.md) | Optional | A list of issuers for this payment method. | getIssuers(): ?array | setIssuers(?array issuers): void |
| `name` | `?string` | Optional | The displayable name of this payment method. | getName(): ?string | setName(?string name): void |
| `promoted` | `?bool` | Optional | Indicates whether this payment method should be promoted or not. | getPromoted(): ?bool | setPromoted(?bool promoted): void |
| `type` | `?string` | Optional | The unique payment method code. | getType(): ?string | setType(?string type): void |

## Example (as JSON)

```json
{
  "apps": [
    {
      "id": "id6",
      "name": "name6"
    },
    {
      "id": "id6",
      "name": "name6"
    },
    {
      "id": "id6",
      "name": "name6"
    }
  ],
  "brand": "brand8",
  "brands": [
    "brands5",
    "brands6"
  ],
  "configuration": {
    "key0": "configuration0"
  },
  "fundingSource": "credit"
}
```

