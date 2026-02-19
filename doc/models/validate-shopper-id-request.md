
# Validate Shopper Id Request

*This model accepts additional fields of type array.*

## Structure

`ValidateShopperIdRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `merchantAccount` | `string` | Required | The merchant account identifier, with which you want to process the transaction.<br><br>**Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1000` | getMerchantAccount(): string | setMerchantAccount(string merchantAccount): void |
| `paymentMethod` | [`ShopperIdPaymentMethod1`](../../doc/models/shopper-id-payment-method-1.md) | Required | paymentMethod | getPaymentMethod(): ShopperIdPaymentMethod1 | setPaymentMethod(ShopperIdPaymentMethod1 paymentMethod): void |
| `shopperEmail` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `300` | getShopperEmail(): ?string | setShopperEmail(?string shopperEmail): void |
| `shopperIp` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `15` | getShopperIp(): ?string | setShopperIp(?string shopperIp): void |
| `shopperReference` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` | getShopperReference(): ?string | setShopperReference(?string shopperReference): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "merchantAccount": "merchantAccount8",
  "paymentMethod": {
    "type": "ShopperIdPaymentMethod1",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "shopperEmail": "shopperEmail0",
  "shopperIP": "shopperIP4",
  "shopperReference": "shopperReference4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

