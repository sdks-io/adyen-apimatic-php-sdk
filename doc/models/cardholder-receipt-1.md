
# Cardholder Receipt 1

Settings to define the header of the shopper receipt.

## Structure

`CardholderReceipt1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `headerForAuthorizedReceipt` | `?string` | Optional | The structure of the header to show on the shopper receipt. You can define the order of one or two header lines and blank lines. For example, **header1,header2,filler**. The text of the header lines is defined in the Customer Area under **In-person payments** > **Terminal settings** > **Receipts** in the **Receipt lines** block. | getHeaderForAuthorizedReceipt(): ?string | setHeaderForAuthorizedReceipt(?string headerForAuthorizedReceipt): void |

## Example (as JSON)

```json
{
  "headerForAuthorizedReceipt": "headerForAuthorizedReceipt8"
}
```

