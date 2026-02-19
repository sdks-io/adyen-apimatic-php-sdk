
# Paypal Update Order Response

## Structure

`PaypalUpdateOrderResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `paymentData` | `string` | Required | The updated paymentData. | getPaymentData(): string | setPaymentData(string paymentData): void |
| `status` | [`string(Status3)`](../../doc/models/status-3.md) | Required | The status of the request. This indicates whether the order was successfully updated with PayPal. | getStatus(): string | setStatus(string status): void |

## Example (as JSON)

```json
{
  "paymentData": "paymentData0",
  "status": "error"
}
```

