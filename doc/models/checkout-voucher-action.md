
# Checkout Voucher Action

## Structure

`CheckoutVoucherAction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `alternativeReference` | `?string` | Optional | The voucher alternative reference code. | getAlternativeReference(): ?string | setAlternativeReference(?string alternativeReference): void |
| `collectionInstitutionNumber` | `?string` | Optional | A collection institution number (store number) for Econtext Pay-Easy ATM. | getCollectionInstitutionNumber(): ?string | setCollectionInstitutionNumber(?string collectionInstitutionNumber): void |
| `downloadUrl` | `?string` | Optional | The URL to download the voucher. | getDownloadUrl(): ?string | setDownloadUrl(?string downloadUrl): void |
| `entity` | `?string` | Optional | An entity number of Multibanco. | getEntity(): ?string | setEntity(?string entity): void |
| `expiresAt` | `?string` | Optional | The date time of the voucher expiry. | getExpiresAt(): ?string | setExpiresAt(?string expiresAt): void |
| `initialAmount` | [`?Amount13`](../../doc/models/amount-13.md) | Optional | The initial amount. | getInitialAmount(): ?Amount13 | setInitialAmount(?Amount13 initialAmount): void |
| `instructionsUrl` | `?string` | Optional | The URL to the detailed instructions to make payment using the voucher. | getInstructionsUrl(): ?string | setInstructionsUrl(?string instructionsUrl): void |
| `issuer` | `?string` | Optional | The issuer of the voucher. | getIssuer(): ?string | setIssuer(?string issuer): void |
| `maskedTelephoneNumber` | `?string` | Optional | The shopper telephone number (partially masked). | getMaskedTelephoneNumber(): ?string | setMaskedTelephoneNumber(?string maskedTelephoneNumber): void |
| `merchantName` | `?string` | Optional | The merchant name. | getMerchantName(): ?string | setMerchantName(?string merchantName): void |
| `merchantReference` | `?string` | Optional | The merchant reference. | getMerchantReference(): ?string | setMerchantReference(?string merchantReference): void |
| `passCreationToken` | `?string` | Optional | A Base64-encoded token containing all properties of the voucher. For iOS, you can use this to pass a voucher to Apple Wallet. | getPassCreationToken(): ?string | setPassCreationToken(?string passCreationToken): void |
| `paymentData` | `?string` | Optional | Encoded payment data. | getPaymentData(): ?string | setPaymentData(?string paymentData): void |
| `paymentMethodType` | `?string` | Optional | Specifies the payment method. | getPaymentMethodType(): ?string | setPaymentMethodType(?string paymentMethodType): void |
| `reference` | `?string` | Optional | The voucher reference code. | getReference(): ?string | setReference(?string reference): void |
| `shopperEmail` | `?string` | Optional | The shopper email. | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `shopperName` | `?string` | Optional | The shopper name. | getShopperName(): ?string | setShopperName(?string shopperName): void |
| `surcharge` | [`?Amount14`](../../doc/models/amount-14.md) | Optional | The surcharge amount. | getSurcharge(): ?Amount14 | setSurcharge(?Amount14 surcharge): void |
| `totalAmount` | [`?Amount15`](../../doc/models/amount-15.md) | Optional | The total amount (initial plus surcharge amount). | getTotalAmount(): ?Amount15 | setTotalAmount(?Amount15 totalAmount): void |
| `type` | `string` | Required, Constant | **voucher**<br><br>**Value**: `'voucher'` | getType(): string | setType(string type): void |
| `url` | `?string` | Optional | Specifies the URL to redirect to. | getUrl(): ?string | setUrl(?string url): void |

## Example (as JSON)

```json
{
  "type": "voucher",
  "alternativeReference": "alternativeReference4",
  "collectionInstitutionNumber": "collectionInstitutionNumber2",
  "downloadUrl": "downloadUrl4",
  "entity": "entity4",
  "expiresAt": "expiresAt2"
}
```

