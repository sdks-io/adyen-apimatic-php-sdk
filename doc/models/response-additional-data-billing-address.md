
# Response Additional Data Billing Address

## Structure

`ResponseAdditionalDataBillingAddress`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingAddressCity` | `?string` | Optional | The billing address city passed in the payment request. | getBillingAddressCity(): ?string | setBillingAddressCity(?string billingAddressCity): void |
| `billingAddressCountry` | `?string` | Optional | The billing address country passed in the payment request.<br><br>Example: NL | getBillingAddressCountry(): ?string | setBillingAddressCountry(?string billingAddressCountry): void |
| `billingAddressHouseNumberOrName` | `?string` | Optional | The billing address house number or name passed in the payment request. | getBillingAddressHouseNumberOrName(): ?string | setBillingAddressHouseNumberOrName(?string billingAddressHouseNumberOrName): void |
| `billingAddressPostalCode` | `?string` | Optional | The billing address postal code passed in the payment request.<br><br>Example: 1011 DJ | getBillingAddressPostalCode(): ?string | setBillingAddressPostalCode(?string billingAddressPostalCode): void |
| `billingAddressStateOrProvince` | `?string` | Optional | The billing address state or province passed in the payment request.<br><br>Example: NH | getBillingAddressStateOrProvince(): ?string | setBillingAddressStateOrProvince(?string billingAddressStateOrProvince): void |
| `billingAddressStreet` | `?string` | Optional | The billing address street passed in the payment request. | getBillingAddressStreet(): ?string | setBillingAddressStreet(?string billingAddressStreet): void |

## Example (as JSON)

```json
{
  "billingAddress.city": "billingAddress.city8",
  "billingAddress.country": "billingAddress.country2",
  "billingAddress.houseNumberOrName": "billingAddress.houseNumberOrName6",
  "billingAddress.postalCode": "billingAddress.postalCode4",
  "billingAddress.stateOrProvince": "billingAddress.stateOrProvince4"
}
```

