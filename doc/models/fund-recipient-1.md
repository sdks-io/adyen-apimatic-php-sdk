
# Fund Recipient 1

the person or entity receiving the money

## Structure

`FundRecipient1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `iban` | `?string` | Optional | The IBAN of the bank account where the funds are being transferred to. | getIban(): ?string | setIban(?string iban): void |
| `billingAddress` | [`?Address3`](../../doc/models/address-3.md) | Optional | The address where to send the invoice. | getBillingAddress(): ?Address3 | setBillingAddress(?Address3 billingAddress): void |
| `paymentMethod` | [`?Card2`](../../doc/models/card-2.md) | Optional | The payment method used by the shopper. | getPaymentMethod(): ?Card2 | setPaymentMethod(?Card2 paymentMethod): void |
| `shopperEmail` | `?string` | Optional | The email address of the shopper. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `shopperName` | [`?Name2`](../../doc/models/name-2.md) | Optional | The name of the shopper. | getShopperName(): ?Name2 | setShopperName(?Name2 shopperName): void |
| `shopperReference` | `?string` | Optional | Required for recurring payments.<br>Your reference to uniquely identify this shopper, for example user ID or account ID. The value is case-sensitive and must be at least three characters.<br><br>> Your reference must not include personally identifiable information (PII) such as name or email address.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `256` | getShopperReference(): ?string | setShopperReference(?string shopperReference): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `subMerchant` | [`?SubMerchant2`](../../doc/models/sub-merchant-2.md) | Optional | Required for back-to-back/purchase-driven-load transactions, where the funds are taken from the shopper's stored card when the wallet balance is insufficient.<br>The final merchant who will receive the money, also known as a [sub-merchant](https://docs.adyen.com/get-started-with-adyen/payment-glossary/#submerchant). | getSubMerchant(): ?SubMerchant2 | setSubMerchant(?SubMerchant2 subMerchant): void |
| `telephoneNumber` | `?string` | Optional | The telephone number of the shopper. | getTelephoneNumber(): ?string | setTelephoneNumber(?string telephoneNumber): void |
| `walletIdentifier` | `?string` | Optional | The unique identifier for the wallet the funds are being transferred to. You can use the shopper reference or any other identifier. | getWalletIdentifier(): ?string | setWalletIdentifier(?string walletIdentifier): void |
| `walletOwnerTaxId` | `?string` | Optional | The tax identifier of the person receiving the funds. | getWalletOwnerTaxId(): ?string | setWalletOwnerTaxId(?string walletOwnerTaxId): void |
| `walletPurpose` | [`?string(WalletPurpose)`](../../doc/models/wallet-purpose.md) | Optional | The purpose of a digital wallet transaction. | getWalletPurpose(): ?string | setWalletPurpose(?string walletPurpose): void |

## Example (as JSON)

```json
{
  "IBAN": "IBAN8",
  "billingAddress": {
    "city": "city8",
    "country": "country6",
    "houseNumberOrName": "houseNumberOrName0",
    "postalCode": "postalCode6",
    "stateOrProvince": "stateOrProvince0",
    "street": "street2"
  },
  "paymentMethod": {
    "billingSequenceNumber": "billingSequenceNumber2",
    "brand": "brand6",
    "checkoutAttemptId": "checkoutAttemptId8",
    "cupsecureplus.smscode": "cupsecureplus.smscode0",
    "cvc": "cvc6"
  },
  "shopperEmail": "shopperEmail8",
  "shopperName": {
    "firstName": "firstName2",
    "lastName": "lastName6"
  }
}
```

