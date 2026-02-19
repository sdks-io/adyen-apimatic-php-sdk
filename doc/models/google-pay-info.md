
# Google Pay Info

## Structure

`GooglePayInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantId` | `string` | Required | Google Pay [Merchant ID](https://support.google.com/paymentscenter/answer/7163092?hl=en). Character length and limitations: 16 alphanumeric characters or 20 numeric characters.<br><br>**Constraints**: *Minimum Length*: `16`, *Maximum Length*: `20` | getMerchantId(): string | setMerchantId(string merchantId): void |
| `reuseMerchantId` | `?bool` | Optional | Indicates whether the Google Pay Merchant ID is used for several merchant accounts. Default value: **false**. | getReuseMerchantId(): ?bool | setReuseMerchantId(?bool reuseMerchantId): void |

## Example (as JSON)

```json
{
  "merchantId": "merchantId4",
  "reuseMerchantId": false
}
```

