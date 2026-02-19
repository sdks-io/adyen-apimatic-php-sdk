
# Merchant

## Structure

`Merchant`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?MerchantLinks2`](../../doc/models/merchant-links-2.md) | Optional | References to resources connected with this merchant. | getLinks(): ?MerchantLinks2 | setLinks(?MerchantLinks2 links): void |
| `captureDelay` | `?string` | Optional | The [capture delay](https://docs.adyen.com/online-payments/capture#capture-delay) set for the merchant account.<br><br>Possible values:<br><br>* **Immediate**<br>* **Manual**<br>* Number of days from **1** to **29** | getCaptureDelay(): ?string | setCaptureDelay(?string captureDelay): void |
| `companyId` | `?string` | Optional | The unique identifier of the company account this merchant belongs to | getCompanyId(): ?string | setCompanyId(?string companyId): void |
| `dataCenters` | [`?(DataCenter[])`](../../doc/models/data-center.md) | Optional | List of available data centers.<br><br>Adyen has several data centers around the world.In the URL that you use for making API requests, we recommend you use the live URL prefix from the data center closest to your shoppers. | getDataCenters(): ?array | setDataCenters(?array dataCenters): void |
| `defaultShopperInteraction` | `?string` | Optional | The default [`shopperInteraction`](https://docs.adyen.com/api-explorer/#/CheckoutService/v68/post/payments__reqParam_shopperInteraction) value used when processing payments through this merchant account. | getDefaultShopperInteraction(): ?string | setDefaultShopperInteraction(?string defaultShopperInteraction): void |
| `description` | `?string` | Optional | Your description for the merchant account, maximum 300 characters | getDescription(): ?string | setDescription(?string description): void |
| `id` | `?string` | Optional | The unique identifier of the merchant account. | getId(): ?string | setId(?string id): void |
| `merchantCity` | `?string` | Optional | The city where the legal entity of this merchant account is registered. | getMerchantCity(): ?string | setMerchantCity(?string merchantCity): void |
| `name` | `?string` | Optional | The name of the legal entity associated with the merchant account. | getName(): ?string | setName(?string name): void |
| `pricingPlan` | `?string` | Optional | Only applies to merchant accounts managed by Adyen's partners. The name of the pricing plan assigned to the merchant account. | getPricingPlan(): ?string | setPricingPlan(?string pricingPlan): void |
| `primarySettlementCurrency` | `?string` | Optional | The currency of the country where the legal entity of this merchant account is registered. Format: [ISO currency code](https://docs.adyen.com/development-resources/currency-codes). For example, a legal entity based in the United States has USD as the primary settlement currency. | getPrimarySettlementCurrency(): ?string | setPrimarySettlementCurrency(?string primarySettlementCurrency): void |
| `reference` | `?string` | Optional | Reference of the merchant account. | getReference(): ?string | setReference(?string reference): void |
| `shopWebAddress` | `?string` | Optional | The URL for the ecommerce website used with this merchant account. | getShopWebAddress(): ?string | setShopWebAddress(?string shopWebAddress): void |
| `status` | `?string` | Optional | The status of the merchant account.<br><br>Possible values:<br><br>* **PreActive**: The merchant account has been created. Users cannot access the merchant account in the Customer Area. The account cannot process payments.<br>* **Active**: Users can access the merchant account in the Customer Area. If the company account is also **Active**, then payment processing and payouts are enabled.<br>* **InactiveWithModifications**: Users can access the merchant account in the Customer Area. You cannot process new payments but you can still modify payments, for example issue refunds. You can still receive payouts.<br>* **Inactive**: Users can access the merchant account in the Customer Area. Payment processing and payouts are disabled.<br>* **Closed**: The account is closed and this cannot be reversed. Users cannot log in. Payment processing and payouts are disabled. | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
{
  "_links": {
    "apiCredentials": {
      "href": "href8"
    },
    "self": {
      "href": "href0"
    },
    "users": {
      "href": "href8"
    },
    "webhooks": {
      "href": "href8"
    }
  },
  "captureDelay": "captureDelay8",
  "companyId": "companyId2",
  "dataCenters": [
    {
      "livePrefix": "livePrefix4",
      "name": "name6"
    }
  ],
  "defaultShopperInteraction": "defaultShopperInteraction0"
}
```

