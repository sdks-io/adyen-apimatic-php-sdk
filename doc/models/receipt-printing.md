
# Receipt Printing

## Structure

`ReceiptPrinting`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantApproved` | `?bool` | Optional | Print a merchant receipt when the payment is approved. | getMerchantApproved(): ?bool | setMerchantApproved(?bool merchantApproved): void |
| `merchantCancelled` | `?bool` | Optional | Print a merchant receipt when the transaction is cancelled. | getMerchantCancelled(): ?bool | setMerchantCancelled(?bool merchantCancelled): void |
| `merchantCaptureApproved` | `?bool` | Optional | Print a merchant receipt when capturing the payment is approved. | getMerchantCaptureApproved(): ?bool | setMerchantCaptureApproved(?bool merchantCaptureApproved): void |
| `merchantCaptureRefused` | `?bool` | Optional | Print a merchant receipt when capturing the payment is refused. | getMerchantCaptureRefused(): ?bool | setMerchantCaptureRefused(?bool merchantCaptureRefused): void |
| `merchantRefundApproved` | `?bool` | Optional | Print a merchant receipt when the refund is approved. | getMerchantRefundApproved(): ?bool | setMerchantRefundApproved(?bool merchantRefundApproved): void |
| `merchantRefundRefused` | `?bool` | Optional | Print a merchant receipt when the refund is refused. | getMerchantRefundRefused(): ?bool | setMerchantRefundRefused(?bool merchantRefundRefused): void |
| `merchantRefused` | `?bool` | Optional | Print a merchant receipt when the payment is refused. | getMerchantRefused(): ?bool | setMerchantRefused(?bool merchantRefused): void |
| `merchantVoid` | `?bool` | Optional | Print a merchant receipt when a previous transaction is voided. | getMerchantVoid(): ?bool | setMerchantVoid(?bool merchantVoid): void |
| `shopperApproved` | `?bool` | Optional | Print a shopper receipt when the payment is approved. | getShopperApproved(): ?bool | setShopperApproved(?bool shopperApproved): void |
| `shopperCancelled` | `?bool` | Optional | Print a shopper receipt when the transaction is cancelled. | getShopperCancelled(): ?bool | setShopperCancelled(?bool shopperCancelled): void |
| `shopperCaptureApproved` | `?bool` | Optional | Print a shopper receipt when capturing the payment is approved. | getShopperCaptureApproved(): ?bool | setShopperCaptureApproved(?bool shopperCaptureApproved): void |
| `shopperCaptureRefused` | `?bool` | Optional | Print a shopper receipt when capturing the payment is refused. | getShopperCaptureRefused(): ?bool | setShopperCaptureRefused(?bool shopperCaptureRefused): void |
| `shopperRefundApproved` | `?bool` | Optional | Print a shopper receipt when the refund is approved. | getShopperRefundApproved(): ?bool | setShopperRefundApproved(?bool shopperRefundApproved): void |
| `shopperRefundRefused` | `?bool` | Optional | Print a shopper receipt when the refund is refused. | getShopperRefundRefused(): ?bool | setShopperRefundRefused(?bool shopperRefundRefused): void |
| `shopperRefused` | `?bool` | Optional | Print a shopper receipt when the payment is refused. | getShopperRefused(): ?bool | setShopperRefused(?bool shopperRefused): void |
| `shopperVoid` | `?bool` | Optional | Print a shopper receipt when a previous transaction is voided. | getShopperVoid(): ?bool | setShopperVoid(?bool shopperVoid): void |

## Example (as JSON)

```json
{
  "merchantApproved": false,
  "merchantCancelled": false,
  "merchantCaptureApproved": false,
  "merchantCaptureRefused": false,
  "merchantRefundApproved": false
}
```

