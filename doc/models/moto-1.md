
# Moto 1

Settings for Mail Order/Telephone Order transactions.

## Structure

`Moto1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enableMoto` | `?bool` | Optional | Enable MOTO transactions. | getEnableMoto(): ?bool | setEnableMoto(?bool enableMoto): void |
| `maxAmount` | `?int` | Optional | The maximum amount for MOTO transactions. You need to set the currency for this amount using the [`standalone.currencyCode`](https://docs.adyen.com/api-explorer/Management/1/patch/companies/(companyId)/terminalSettings#request-standalone-currencyCode) parameter. Do not enable standalone, unless you are using a standalone solution. | getMaxAmount(): ?int | setMaxAmount(?int maxAmount): void |

## Example (as JSON)

```json
{
  "enableMoto": false,
  "maxAmount": 250
}
```

