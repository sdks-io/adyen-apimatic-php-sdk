
# Cartes Bancaires Info 1

Details to provide if `type` is **cartebancaire**.

## Structure

`CartesBancairesInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `siret` | `string` | Required | Cartes Bancaires SIRET. Format: 14 digits. | getSiret(): string | setSiret(string siret): void |
| `transactionDescription` | [`?TransactionDescriptionInfo1`](../../doc/models/transaction-description-info-1.md) | Optional | Information regarding the transaction description.<br><br>> You cannot configure the transaction description in the test environment. | getTransactionDescription(): ?TransactionDescriptionInfo1 | setTransactionDescription(?TransactionDescriptionInfo1 transactionDescription): void |

## Example (as JSON)

```json
{
  "siret": "siret2",
  "transactionDescription": {
    "doingBusinessAsName": "doingBusinessAsName0",
    "type": "fixed"
  }
}
```

