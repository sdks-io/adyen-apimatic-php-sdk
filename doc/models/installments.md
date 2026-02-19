
# Installments

## Structure

`Installments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `extra` | `?int` | Optional | Defines the bonus percentage, refund percentage or if the transaction is Buy now Pay later.<br>Used for [card installments in Mexico](https://docs.adyen.com/payment-methods/cards/credit-card-installments/#getting-paid-mexico) | getExtra(): ?int | setExtra(?int extra): void |
| `plan` | [`?string(Plan)`](../../doc/models/plan.md) | Optional | The installment plan, used for [card installments in Japan](https://docs.adyen.com/payment-methods/cards/credit-card-installments#make-a-payment-japan).<br>and [Mexico](https://docs.adyen.com/payment-methods/cards/credit-card-installments/#getting-paid-mexico).<br>By default, this is set to **regular**. | getPlan(): ?string | setPlan(?string plan): void |
| `value` | `int` | Required | Defines the number of installments.<br>Usually, the maximum allowed number of installments is capped. For example, it may not be possible to split a payment in more than 24 installments. The acquirer sets this upper limit, so its value may vary.<br>This value can be zero for Installments processed in Mexico. | getValue(): int | setValue(int value): void |

## Example (as JSON)

```json
{
  "extra": 184,
  "plan": "nointeres_refund_prctg",
  "value": 180
}
```

