
# Agency

## Structure

`Agency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `invoiceNumber` | `?string` | Optional | The reference number for the invoice, issued by the agency.<br><br>* Encoding: ASCII<br>* minLength: 1 character<br>* maxLength: 6 characters | getInvoiceNumber(): ?string | setInvoiceNumber(?string invoiceNumber): void |
| `planName` | `?string` | Optional | The two-letter agency plan identifier.<br><br>* Encoding: ASCII<br>* minLength: 2 characters<br>* maxLength: 2 characters | getPlanName(): ?string | setPlanName(?string planName): void |

## Example (as JSON)

```json
{
  "invoiceNumber": "invoiceNumber6",
  "planName": "planName6"
}
```

