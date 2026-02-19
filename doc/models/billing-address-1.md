
# Billing Address 1

The address where to send the invoice.

## Structure

`BillingAddress1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `city` | `string` | Required | The name of the city. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` | getCity(): string | setCity(string city): void |
| `country` | `string` | Required | The two-character ISO-3166-1 alpha-2 country code. For example, **US**.<br><br>> If you don't know the country or are not collecting the country from the shopper, provide `country` as `ZZ`. | getCountry(): string | setCountry(string country): void |
| `houseNumberOrName` | `string` | Required | The number or name of the house. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` | getHouseNumberOrName(): string | setHouseNumberOrName(string houseNumberOrName): void |
| `postalCode` | `string` | Required | A maximum of five digits for an address in the US, or a maximum of ten characters for an address in all other countries. | getPostalCode(): string | setPostalCode(string postalCode): void |
| `stateOrProvince` | `?string` | Optional | The two-character ISO 3166-2 state or province code. For example, **CA** in the US or **ON** in Canada.<br><br>> Required for the US and Canada.<br><br>**Constraints**: *Maximum Length*: `1000` | getStateOrProvince(): ?string | setStateOrProvince(?string stateOrProvince): void |
| `street` | `string` | Required | The name of the street. Maximum length: 3000 characters.<br><br>> The house number should not be included in this field; it should be separately provided via `houseNumberOrName`.<br><br>**Constraints**: *Maximum Length*: `3000` | getStreet(): string | setStreet(string street): void |

## Example (as JSON)

```json
{
  "city": "city4",
  "country": "country0",
  "houseNumberOrName": "houseNumberOrName4",
  "postalCode": "postalCode2",
  "stateOrProvince": "stateOrProvince4",
  "street": "street6"
}
```

