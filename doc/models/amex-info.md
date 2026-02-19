
# Amex Info

## Structure

`AmexInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `midNumber` | `?string` | Optional | Merchant ID (MID) number. Format: 10 numeric characters.<br>You must provide this field when you request `gatewayContract` or `paymentDesignatorContract` service levels.<br><br>**Constraints**: *Maximum Length*: `10` | getMidNumber(): ?string | setMidNumber(?string midNumber): void |
| `reuseMidNumber` | `?bool` | Optional | Indicates whether the Amex Merchant ID is reused from a previously setup Amex payment method.<br>This is only applicable for `gatewayContract` and `paymentDesignatorContract` service levels.<br>The default value is **false**.<br><br>**Default**: `false` | getReuseMidNumber(): ?bool | setReuseMidNumber(?bool reuseMidNumber): void |
| `serviceLevel` | [`string(ServiceLevel)`](../../doc/models/service-level.md) | Required | Specifies the service level (settlement type) of this payment method. Possible values:<br><br>* **noContract**: Adyen holds the contract with American Express.<br>* **gatewayContract**: American Express receives the settlement and handles disputes, then pays out to you or your sub-merchant directly.<br>* **paymentDesignatorContract**: Adyen receives the settlement, and handles disputes and payouts. | getServiceLevel(): string | setServiceLevel(string serviceLevel): void |

## Example (as JSON)

```json
{
  "reuseMidNumber": false,
  "serviceLevel": "noContract",
  "midNumber": "midNumber0"
}
```

