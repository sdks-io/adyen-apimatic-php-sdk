
# Split Configuration Logic

## Structure

`SplitConfigurationLogic`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `acquiringFees` | [`?string(AcquiringFees)`](../../doc/models/acquiring-fees.md) | Optional | Deducts the acquiring fees (the aggregated amount of interchange and scheme fee) from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getAcquiringFees(): ?string | setAcquiringFees(?string acquiringFees): void |
| `additionalCommission` | [`?AdditionalCommission1`](../../doc/models/additional-commission-1.md) | Optional | Defines whether to book an additional commission for payments to your user's balance account. The commission amount can be defined as a fixed amount (specified in minor units), a percentage (specified in basis points), or both. | getAdditionalCommission(): ?AdditionalCommission1 | setAdditionalCommission(?AdditionalCommission1 additionalCommission): void |
| `adyenCommission` | [`?string(AdyenCommission)`](../../doc/models/adyen-commission.md) | Optional | Deducts the transaction fee due to Adyen under [blended rates](https://www.adyen.com/knowledge-hub/guides/payments-training-guide/get-the-best-from-your-card-processing) from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getAdyenCommission(): ?string | setAdyenCommission(?string adyenCommission): void |
| `adyenFees` | [`?string(AdyenFees)`](../../doc/models/adyen-fees.md) | Optional | Deducts the fees due to Adyen (markup or commission) from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getAdyenFees(): ?string | setAdyenFees(?string adyenFees): void |
| `adyenMarkup` | [`?string(AdyenMarkup)`](../../doc/models/adyen-markup.md) | Optional | Deducts the transaction fee due to Adyen under [Interchange ++ pricing](https://www.adyen.com/what-is-interchange) from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getAdyenMarkup(): ?string | setAdyenMarkup(?string adyenMarkup): void |
| `chargeback` | [`?string(Behavior)`](../../doc/models/behavior.md) | Optional | Specifies how and from which balance account(s) to deduct the chargeback amount.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**, **deductAccordingToSplitRatio**. | getChargeback(): ?string | setChargeback(?string chargeback): void |
| `chargebackCostAllocation` | [`?string(ChargebackCostAllocation)`](../../doc/models/chargeback-cost-allocation.md) | Optional | Deducts the chargeback costs from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount** | getChargebackCostAllocation(): ?string | setChargebackCostAllocation(?string chargebackCostAllocation): void |
| `commission` | [`Commission1`](../../doc/models/commission-1.md) | Required | Defines your platform's commission for the processed payments as a fixed amount (specified in minor units), a percentage (specified in basis points), or both. The commission is booked to your platform's liable balance account. | getCommission(): Commission1 | setCommission(Commission1 commission): void |
| `interchange` | [`?string(Interchange)`](../../doc/models/interchange.md) | Optional | Deducts the interchange fee from specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getInterchange(): ?string | setInterchange(?string interchange): void |
| `paymentFee` | [`?string(PaymentFee)`](../../doc/models/payment-fee.md) | Optional | Deducts all transaction fees incurred by the payment from the specified balance account. The transaction fees include the acquiring fees (interchange and scheme fee), and the fees due to Adyen (markup or commission). You can book any and all these fees to different balance account by specifying other transaction fee parameters in your split configuration profile:<br><br>- [`adyenCommission`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-adyenCommission): The transaction fee due to Adyen under [blended rates](https://www.adyen.com/knowledge-hub/interchange-fees-explained#interchange-vs-blended).<br>- [`adyenMarkup`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-adyenMarkup): The transaction fee due to Adyen under [Interchange ++ pricing](https://www.adyen.com/knowledge-hub/interchange-fees-explained#interchange-vs-blended).<br>- [`schemeFee`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-schemeFee): The fee paid to the card scheme for using their network.<br>- [`interchange`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-interchange): The fee paid to the issuer for each payment transaction made with the card network.<br>- [`adyenFees`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-adyenFees): The aggregated amount of Adyen's commission and markup.<br>- [`acquiringFees`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/splitConfigurations#request-rules-splitLogic-acquiringFees): The aggregated amount of the interchange and scheme fees.<br><br>If you don't include at least one transaction fee type in the `splitLogic` object, Adyen updates the payment request with the `paymentFee` parameter, booking all transaction fees to your platform's liable balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getPaymentFee(): ?string | setPaymentFee(?string paymentFee): void |
| `refund` | [`?string(Behavior)`](../../doc/models/behavior.md) | Optional | Specifies how and from which balance account(s) to deduct the refund amount.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**, **deductAccordingToSplitRatio** | getRefund(): ?string | setRefund(?string refund): void |
| `refundCostAllocation` | [`?string(RefundCostAllocation)`](../../doc/models/refund-cost-allocation.md) | Optional | Deducts the refund costs from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount** | getRefundCostAllocation(): ?string | setRefundCostAllocation(?string refundCostAllocation): void |
| `remainder` | [`?string(Remainder)`](../../doc/models/remainder.md) | Optional | Books the amount left over after currency conversion to the specified balance account.<br><br>Possible values: **addToLiableAccount**, **addToOneBalanceAccount**. | getRemainder(): ?string | setRemainder(?string remainder): void |
| `schemeFee` | [`?string(SchemeFee)`](../../doc/models/scheme-fee.md) | Optional | Deducts the scheme fee from the specified balance account.<br><br>Possible values: **deductFromLiableAccount**, **deductFromOneBalanceAccount**. | getSchemeFee(): ?string | setSchemeFee(?string schemeFee): void |
| `splitLogicId` | `?string` | Optional | Unique identifier of the collection of split instructions that are applied when the rule conditions are met. | getSplitLogicId(): ?string | setSplitLogicId(?string splitLogicId): void |
| `surcharge` | [`?string(Surcharge3)`](../../doc/models/surcharge-3.md) | Optional | Books the surcharge amount to the specified balance account.<br><br>Possible values: **addToLiableAccount**, **addToOneBalanceAccount** | getSurcharge(): ?string | setSurcharge(?string surcharge): void |
| `tip` | [`?string(Tip)`](../../doc/models/tip.md) | Optional | Books the tips (gratuity) to the specified balance account.<br><br>Possible values: **addToLiableAccount**, **addToOneBalanceAccount**. | getTip(): ?string | setTip(?string tip): void |

## Example (as JSON)

```json
{
  "acquiringFees": "deductFromLiableAccount",
  "additionalCommission": {
    "balanceAccountId": "balanceAccountId0",
    "fixedAmount": 100,
    "variablePercentage": 64
  },
  "adyenCommission": "deductFromLiableAccount",
  "adyenFees": "deductFromLiableAccount",
  "adyenMarkup": "deductFromLiableAccount",
  "commission": {
    "fixedAmount": 112,
    "variablePercentage": 52
  }
}
```

