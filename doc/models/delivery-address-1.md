
# Delivery Address 1

The address where the purchased goods should be delivered.

## Structure

`DeliveryAddress1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `city` | `string` | Required | The name of the city. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` | getCity(): string | setCity(string city): void |
| `country` | `string` | Required | The two-character ISO-3166-1 alpha-2 country code. For example, **US**.<br><br>> If you don't know the country or are not collecting the country from the shopper, provide `country` as `ZZ`. | getCountry(): string | setCountry(string country): void |
| `firstName` | `?string` | Optional | - | getFirstName(): ?string | setFirstName(?string firstName): void |
| `houseNumberOrName` | `string` | Required | The number or name of the house. Maximum length: 3000 characters.<br><br>**Constraints**: *Maximum Length*: `3000` | getHouseNumberOrName(): string | setHouseNumberOrName(string houseNumberOrName): void |
| `lastName` | `?string` | Optional | - | getLastName(): ?string | setLastName(?string lastName): void |
| `postalCode` | `string` | Required | A maximum of five digits for an address in the US, or a maximum of ten characters for an address in all other countries. | getPostalCode(): string | setPostalCode(string postalCode): void |
| `stateOrProvince` | `?string` | Optional | The two-character ISO 3166-2 state or province code. For example, **CA** in the US or **ON** in Canada.<br><br>> Required for the US and Canada.<br><br>**Constraints**: *Maximum Length*: `1000` | getStateOrProvince(): ?string | setStateOrProvince(?string stateOrProvince): void |
| `street` | `string` | Required | The name of the street. Maximum length: 3000 characters.<br><br>> The house number should not be included in this field; it should be separately provided via `houseNumberOrName`.<br><br>**Constraints**: *Maximum Length*: `3000` | getStreet(): string | setStreet(string street): void |

## Example (as JSON)

```json
{
  "city": "city0",
  "country": "country4",
  "firstName": "firstName4",
  "houseNumberOrName": "houseNumberOrName8",
  "lastName": "lastName4",
  "postalCode": "postalCode8",
  "stateOrProvince": "stateOrProvince8",
  "street": "street0"
}
```

