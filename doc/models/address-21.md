
# Address 21

The address details of the shipping location.

## Structure

`Address21`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `city` | `?string` | Optional | The name of the city. | getCity(): ?string | setCity(?string city): void |
| `companyName` | `?string` | Optional | The name of the company. | getCompanyName(): ?string | setCompanyName(?string companyName): void |
| `country` | `?string` | Optional | The two-letter country code, in [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. | getCountry(): ?string | setCountry(?string country): void |
| `postalCode` | `?string` | Optional | The postal code. | getPostalCode(): ?string | setPostalCode(?string postalCode): void |
| `stateOrProvince` | `?string` | Optional | The state or province as defined in [ISO 3166-2](https://www.iso.org/standard/72483.html). For example, **ON** for Ontario, Canada.<br><br>Applicable for the following countries:<br><br>- Australia<br>- Brazil<br>- Canada<br>- India<br>- Mexico<br>- New Zealand<br>- United States | getStateOrProvince(): ?string | setStateOrProvince(?string stateOrProvince): void |
| `streetAddress` | `?string` | Optional | The name of the street, and the house or building number. | getStreetAddress(): ?string | setStreetAddress(?string streetAddress): void |
| `streetAddress2` | `?string` | Optional | Additional address details, if any. | getStreetAddress2(): ?string | setStreetAddress2(?string streetAddress2): void |

## Example (as JSON)

```json
{
  "city": "city0",
  "companyName": "companyName2",
  "country": "country4",
  "postalCode": "postalCode8",
  "stateOrProvince": "stateOrProvince8"
}
```

