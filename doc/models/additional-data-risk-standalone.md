
# Additional Data Risk Standalone

## Structure

`AdditionalDataRiskStandalone`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `payPalCountryCode` | `?string` | Optional | Shopper's country of residence in the form of ISO standard 3166 2-character country codes. | getPayPalCountryCode(): ?string | setPayPalCountryCode(?string payPalCountryCode): void |
| `payPalEmailId` | `?string` | Optional | Shopper's email. | getPayPalEmailId(): ?string | setPayPalEmailId(?string payPalEmailId): void |
| `payPalFirstName` | `?string` | Optional | Shopper's first name. | getPayPalFirstName(): ?string | setPayPalFirstName(?string payPalFirstName): void |
| `payPalLastName` | `?string` | Optional | Shopper's last name. | getPayPalLastName(): ?string | setPayPalLastName(?string payPalLastName): void |
| `payPalPayerId` | `?string` | Optional | Unique PayPal Customer Account identification number. Character length and limitations: 13 single-byte alphanumeric characters. | getPayPalPayerId(): ?string | setPayPalPayerId(?string payPalPayerId): void |
| `payPalPhone` | `?string` | Optional | Shopper's phone number. | getPayPalPhone(): ?string | setPayPalPhone(?string payPalPhone): void |
| `payPalProtectionEligibility` | `?string` | Optional | Allowed values:<br><br>* **Eligible** — Merchant is protected by PayPal's Seller Protection Policy for Unauthorized Payments and Item Not Received.<br><br>* **PartiallyEligible** — Merchant is protected by PayPal's Seller Protection Policy for Item Not Received.<br><br>* **Ineligible** — Merchant is not protected under the Seller Protection Policy. | getPayPalProtectionEligibility(): ?string | setPayPalProtectionEligibility(?string payPalProtectionEligibility): void |
| `payPalTransactionId` | `?string` | Optional | Unique transaction ID of the payment. | getPayPalTransactionId(): ?string | setPayPalTransactionId(?string payPalTransactionId): void |
| `avsResultRaw` | `?string` | Optional | Raw AVS result received from the acquirer, where available. Example: D | getAvsResultRaw(): ?string | setAvsResultRaw(?string avsResultRaw): void |
| `bin` | `?string` | Optional | The Bank Identification Number of a credit card, which is the first six digits of a card number. Required for [tokenized card request](https://docs.adyen.com/online-payments/tokenization). | getBin(): ?string | setBin(?string bin): void |
| `cvcResultRaw` | `?string` | Optional | Raw CVC result received from the acquirer, where available. Example: 1 | getCvcResultRaw(): ?string | setCvcResultRaw(?string cvcResultRaw): void |
| `riskToken` | `?string` | Optional | Unique identifier or token for the shopper's card details. | getRiskToken(): ?string | setRiskToken(?string riskToken): void |
| `threeDAuthenticated` | `?string` | Optional | A Boolean value indicating whether 3DS authentication was completed on this payment. Example: true | getThreeDAuthenticated(): ?string | setThreeDAuthenticated(?string threeDAuthenticated): void |
| `threeDOffered` | `?string` | Optional | A Boolean value indicating whether 3DS was offered for this payment. Example: true | getThreeDOffered(): ?string | setThreeDOffered(?string threeDOffered): void |
| `tokenDataType` | `?string` | Optional | Required for PayPal payments only. The only supported value is: **paypal**. | getTokenDataType(): ?string | setTokenDataType(?string tokenDataType): void |

## Example (as JSON)

```json
{
  "PayPal.CountryCode": "PayPal.CountryCode0",
  "PayPal.EmailId": "PayPal.EmailId0",
  "PayPal.FirstName": "PayPal.FirstName4",
  "PayPal.LastName": "PayPal.LastName0",
  "PayPal.PayerId": "PayPal.PayerId8"
}
```

