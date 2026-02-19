
# Terminal Reassignment Request

## Structure

`TerminalReassignmentRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `companyId` | `?string` | Optional | The unique identifier of the company account to which the terminal is reassigned. | getCompanyId(): ?string | setCompanyId(?string companyId): void |
| `inventory` | `?bool` | Optional | Must be specified when reassigning terminals to a merchant account:<br><br>- If set to **true**, reassigns terminals to the inventory of the merchant account and the terminals cannot process transactions.<br><br>- If set to **false**, reassigns terminals directly to the merchant account and the terminals can process transactions. | getInventory(): ?bool | setInventory(?bool inventory): void |
| `merchantId` | `?string` | Optional | The unique identifier of the merchant account to which the terminal is reassigned. When reassigning terminals to a merchant account, you must specify the `inventory` field. | getMerchantId(): ?string | setMerchantId(?string merchantId): void |
| `storeId` | `?string` | Optional | The unique identifier of the store to which the terminal is reassigned. | getStoreId(): ?string | setStoreId(?string storeId): void |

## Example (as JSON)

```json
{
  "companyId": "companyId0",
  "inventory": false,
  "merchantId": "merchantId6",
  "storeId": "storeId6"
}
```

