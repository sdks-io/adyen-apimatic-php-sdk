
# Checkout Bank Transfer Action

## Structure

`CheckoutBankTransferAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountNumber` | `?string` | Optional | The account number of the bank transfer. | getAccountNumber(): ?string | setAccountNumber(?string accountNumber): void |
| `bankCode` | `?string` | Optional | The bank code of the bank transfer. | getBankCode(): ?string | setBankCode(?string bankCode): void |
| `beneficiary` | `?string` | Optional | The name of the account holder. | getBeneficiary(): ?string | setBeneficiary(?string beneficiary): void |
| `bic` | `?string` | Optional | The BIC of the IBAN. | getBic(): ?string | setBic(?string bic): void |
| `branchCode` | `?string` | Optional | The branch code of the bank transfer. | getBranchCode(): ?string | setBranchCode(?string branchCode): void |
| `downloadUrl` | `?string` | Optional | The url to download payment details with. | getDownloadUrl(): ?string | setDownloadUrl(?string downloadUrl): void |
| `iban` | `?string` | Optional | The IBAN of the bank transfer. | getIban(): ?string | setIban(?string iban): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `reference` | `?string` | Optional | The transfer reference. | getReference(): ?string | setReference(?string reference): void |
| `routingNumber` | `?string` | Optional | The routing number of the bank transfer. | getRoutingNumber(): ?string | setRoutingNumber(?string routingNumber): void |
| `shopperEmail` | `?string` | Optional | The e-mail of the shopper, included if an e-mail was sent to the shopper. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `sortCode` | `?string` | Optional | The sort code of the bank transfer. | getSortCode(): ?string | setSortCode(?string sortCode): void |
| `totalAmount` | [`?Amount10`](../../doc/models/amount-10.md) | Optional | The amount of the bank transfer. | getTotalAmount(): ?Amount10 | setTotalAmount(?Amount10 totalAmount): void |
| `type` | `string` | Required, Constant | The type of the action.<br><br>**Value**: `'bankTransfer'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "bankTransfer",
  "accountNumber": "accountNumber4",
  "bankCode": "bankCode8",
  "beneficiary": "beneficiary6",
  "bic": "bic0",
  "branchCode": "branchCode0"
}
```

