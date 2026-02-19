
# Donation

## Structure

`Donation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes/). | getCurrency(): string | setCurrency(string currency): void |
| `donationType` | `string` | Required | The [type of donation](https://docs.adyen.com/online-payments/donations/#donation-types).<br><br>Possible values:<br><br>* **roundup**: a donation where the original transaction amount is rounded up as a donation.<br>* **fixedAmounts**: a donation where you show fixed donations amounts that the shopper can select from. | getDonationType(): string | setDonationType(string donationType): void |
| `maxRoundupAmount` | `?int` | Optional | The maximum amount a transaction can be rounded up to make a donation. This field is only present when `donationType` is **roundup**. | getMaxRoundupAmount(): ?int | setMaxRoundupAmount(?int maxRoundupAmount): void |
| `type` | `string` | Required | The [type of donation](https://docs.adyen.com/online-payments/donations/#donation-types).<br><br>Possible values:<br><br>* **roundup**: a donation where the original transaction amount is rounded up as a donation.<br>* **fixedAmounts**: a donation where you show fixed donation amounts that the shopper can select from. | getType(): string | setType(string type): void |
| `values` | `?(int[])` | Optional | The fixed donation amounts in [minor units](https://docs.adyen.com/development-resources/currency-codes//#minor-units). This field is only present when `donationType` is **fixedAmounts**. | getValues(): ?array | setValues(?array values): void |

## Example (as JSON)

```json
{
  "currency": "currency2",
  "donationType": "donationType4",
  "maxRoundupAmount": 68,
  "type": "type8",
  "values": [
    136,
    135,
    134
  ]
}
```

