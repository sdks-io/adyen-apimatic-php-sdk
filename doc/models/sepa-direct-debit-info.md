
# Sepa Direct Debit Info

## Structure

`SepaDirectDebitInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `creditorId` | `?string` | Optional | Creditor id | getCreditorId(): ?string | setCreditorId(?string creditorId): void |
| `transactionDescription` | [`?TransactionDescriptionInfo1`](../../doc/models/transaction-description-info-1.md) | Optional | Information regarding the transaction description.<br><br>> You cannot configure the transaction description in the test environment. | getTransactionDescription(): ?TransactionDescriptionInfo1 | setTransactionDescription(?TransactionDescriptionInfo1 transactionDescription): void |

## Example (as JSON)

```json
{
  "creditorId": "creditorId4",
  "transactionDescription": {
    "doingBusinessAsName": "doingBusinessAsName0",
    "type": "fixed"
  }
}
```

