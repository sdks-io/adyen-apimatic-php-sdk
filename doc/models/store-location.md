
# Store Location

## Structure

`StoreLocation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `city` | `?string` | Optional | The name of the city. | getCity(): ?string | setCity(?string city): void |
| `country` | `string` | Required | The two-letter country code in [ISO_3166-1_alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) format. | getCountry(): string | setCountry(string country): void |
| `line1` | `?string` | Optional | The street address. | getLine1(): ?string | setLine1(?string line1): void |
| `line2` | `?string` | Optional | Second address line. | getLine2(): ?string | setLine2(?string line2): void |
| `line3` | `?string` | Optional | Third address line. | getLine3(): ?string | setLine3(?string line3): void |
| `postalCode` | `?string` | Optional | The postal code. | getPostalCode(): ?string | setPostalCode(?string postalCode): void |
| `stateOrProvince` | `?string` | Optional | The state or province code as defined in [ISO 3166-2](https://www.iso.org/standard/72483.html). For example, **ON** for Ontario, Canada.<br><br>Required for the following countries:<br><br>- Australia<br>- Brazil<br>- Canada<br>- India<br>- Mexico<br>- New Zealand<br>- United States | getStateOrProvince(): ?string | setStateOrProvince(?string stateOrProvince): void |

## Example (as JSON)

```json
{
  "city": "city6",
  "country": "country0",
  "line1": "line18",
  "line2": "line20",
  "line3": "line38",
  "postalCode": "postalCode2"
}
```

