
# Cancel Order Response

## Structure

`CancelOrderResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pspReference` | `string` | Required | A unique reference of the cancellation request. | getPspReference(): string | setPspReference(string pspReference): void |
| `resultCode` | `string` | Required, Constant | The result of the cancellation request.<br><br>Possible values:<br><br>* **Received** – Indicates the cancellation has successfully been received by Adyen, and will be processed.<br><br>**Value**: `'Received'` | getResultCode(): string | setResultCode(string resultCode): void |

## Example (as JSON)

```json
{
  "pspReference": "pspReference2",
  "resultCode": "Received"
}
```

