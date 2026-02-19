
# Update Payment Link Request

## Structure

`UpdatePaymentLinkRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `status` | `string` | Required, Constant | Status of the payment link. Possible values:<br><br>* **expired**<br><br>**Value**: `'expired'` | getStatus(): string | setStatus(string status): void |

## Example (as JSON)

```json
{
  "status": "expired"
}
```

