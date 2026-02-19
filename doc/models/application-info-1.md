
# Application Info 1

Information about your application. For more details, see [Building Adyen solutions](https://docs.adyen.com/development-resources/building-adyen-solutions).

## Structure

`ApplicationInfo1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `adyenLibrary` | [`?CommonField4`](../../doc/models/common-field-4.md) | Optional | Adyen-developed software, such as libraries and plugins, used to interact with the Adyen API. For example, Magento plugin, Java API library, etc. | getAdyenLibrary(): ?CommonField4 | setAdyenLibrary(?CommonField4 adyenLibrary): void |
| `adyenPaymentSource` | [`?CommonField1`](../../doc/models/common-field-1.md) | Optional | Adyen-developed software to get payment details. For example, Checkout SDK, Secured Fields SDK, etc. | getAdyenPaymentSource(): ?CommonField1 | setAdyenPaymentSource(?CommonField1 adyenPaymentSource): void |
| `externalPlatform` | [`?ExternalPlatform2`](../../doc/models/external-platform-2.md) | Optional | Third-party developed platform used to initiate payment requests. For example, Magento, Zuora, etc. | getExternalPlatform(): ?ExternalPlatform2 | setExternalPlatform(?ExternalPlatform2 externalPlatform): void |
| `merchantApplication` | [`?CommonField2`](../../doc/models/common-field-2.md) | Optional | Merchant developed software, such as cashier application, used to interact with the Adyen API. | getMerchantApplication(): ?CommonField2 | setMerchantApplication(?CommonField2 merchantApplication): void |
| `merchantDevice` | [`?MerchantDevice2`](../../doc/models/merchant-device-2.md) | Optional | Merchant device information. | getMerchantDevice(): ?MerchantDevice2 | setMerchantDevice(?MerchantDevice2 merchantDevice): void |
| `shopperInteractionDevice` | [`?ShopperInteractionDevice2`](../../doc/models/shopper-interaction-device-2.md) | Optional | Shopper interaction device, such as terminal, mobile device or web browser, to initiate payment requests. | getShopperInteractionDevice(): ?ShopperInteractionDevice2 | setShopperInteractionDevice(?ShopperInteractionDevice2 shopperInteractionDevice): void |

## Example (as JSON)

```json
{
  "adyenLibrary": {
    "name": "name8",
    "version": "version4"
  },
  "adyenPaymentSource": {
    "name": "name2",
    "version": "version8"
  },
  "externalPlatform": {
    "integrator": "integrator0",
    "name": "name4",
    "version": "version0"
  },
  "merchantApplication": {
    "name": "name2",
    "version": "version8"
  },
  "merchantDevice": {
    "os": "os4",
    "osVersion": "osVersion6",
    "reference": "reference8"
  }
}
```

