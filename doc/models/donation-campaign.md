
# Donation Campaign

## Structure

`DonationCampaign`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amounts` | [`?Amounts1`](../../doc/models/amounts-1.md) | Optional | The object that contains the fixed donation amounts that the shopper can select from. | getAmounts(): ?Amounts1 | setAmounts(?Amounts1 amounts): void |
| `bannerUrl` | `?string` | Optional | The URL for the banner of the nonprofit or campaign. | getBannerUrl(): ?string | setBannerUrl(?string bannerUrl): void |
| `campaignName` | `?string` | Optional | The name of the donation campaign.. | getCampaignName(): ?string | setCampaignName(?string campaignName): void |
| `causeName` | `?string` | Optional | The cause of the nonprofit. | getCauseName(): ?string | setCauseName(?string causeName): void |
| `donation` | [`?Donation1`](../../doc/models/donation-1.md) | Optional | The object that contains the details of the donation. | getDonation(): ?Donation1 | setDonation(?Donation1 donation): void |
| `id` | `?string` | Optional | The unique campaign ID of the donation campaign. | getId(): ?string | setId(?string id): void |
| `logoUrl` | `?string` | Optional | The URL for the logo of the nonprofit. | getLogoUrl(): ?string | setLogoUrl(?string logoUrl): void |
| `nonprofitDescription` | `?string` | Optional | The description of the nonprofit. | getNonprofitDescription(): ?string | setNonprofitDescription(?string nonprofitDescription): void |
| `nonprofitName` | `?string` | Optional | The name of the nonprofit organization that receives the donation. | getNonprofitName(): ?string | setNonprofitName(?string nonprofitName): void |
| `nonprofitUrl` | `?string` | Optional | The website URL of the nonprofit. | getNonprofitUrl(): ?string | setNonprofitUrl(?string nonprofitUrl): void |
| `termsAndConditionsUrl` | `?string` | Optional | The URL of the terms and conditions page of the nonprofit and the campaign. | getTermsAndConditionsUrl(): ?string | setTermsAndConditionsUrl(?string termsAndConditionsUrl): void |

## Example (as JSON)

```json
{
  "amounts": {
    "currency": "currency6",
    "values": [
      48,
      49
    ]
  },
  "bannerUrl": "bannerUrl0",
  "campaignName": "campaignName2",
  "causeName": "causeName6",
  "donation": {
    "currency": "currency0",
    "donationType": "donationType2",
    "maxRoundupAmount": 114,
    "type": "type0",
    "values": [
      106,
      105,
      104
    ]
  }
}
```

