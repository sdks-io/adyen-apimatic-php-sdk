
# Terminal Product Price

## Structure

`TerminalProductPrice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `?string` | Optional | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). | getCurrency(): ?string | setCurrency(?string currency): void |
| `value` | `?float` | Optional | The price of the item. | getValue(): ?float | setValue(?float value): void |

## Example (as JSON)

```json
{
  "currency": "currency6",
  "value": 47.38
}
```

