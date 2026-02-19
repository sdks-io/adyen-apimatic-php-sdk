
# Donation Campaigns Request

## Structure

`DonationCampaignsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | The three-character [ISO currency code](https://docs.adyen.com/development-resources/currency-codes/). | getCurrency(): string | setCurrency(string currency): void |
| `locale` | `?string` | Optional | Locale on the shopper interaction device. | getLocale(): ?string | setLocale(?string locale): void |
| `merchantAccount` | `string` | Required | Your merchant account identifier. | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |

## Example (as JSON)

```json
{
  "currency": "currency0",
  "locale": "locale8",
  "merchantAccount": "merchantAccount8"
}
```

