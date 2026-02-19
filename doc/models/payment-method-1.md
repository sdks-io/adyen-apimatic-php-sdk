
# Payment Method 1

## Structure

`PaymentMethod1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accel` | [`?AccelInfo1`](../../doc/models/accel-info-1.md) | Optional | Details to provide if `type` is **accel**. | getAccel(): ?AccelInfo1 | setAccel(?AccelInfo1 accel): void |
| `affirm` | [`?AffirmInfo1`](../../doc/models/affirm-info-1.md) | Optional | Details to provide if `type` is **affirm**. | getAffirm(): ?AffirmInfo1 | setAffirm(?AffirmInfo1 affirm): void |
| `afterpayTouch` | [`?AfterpayTouchInfo1`](../../doc/models/afterpay-touch-info-1.md) | Optional | Details to provide if `type` is **afterpaytouch**. | getAfterpayTouch(): ?AfterpayTouchInfo1 | setAfterpayTouch(?AfterpayTouchInfo1 afterpayTouch): void |
| `alipayPlus` | [`?AlipayPlusInfo1`](../../doc/models/alipay-plus-info-1.md) | Optional | Details to provide if `type` is **alipay_plus**. | getAlipayPlus(): ?AlipayPlusInfo1 | setAlipayPlus(?AlipayPlusInfo1 alipayPlus): void |
| `allowed` | `?bool` | Optional | Indicates whether receiving payments is allowed. This value is set to **true** by Adyen after screening your merchant account. | getAllowed(): ?bool | setAllowed(?bool allowed): void |
| `amex` | [`?AmexInfo1`](../../doc/models/amex-info-1.md) | Optional | Details to provide if `type` is **amex**. | getAmex(): ?AmexInfo1 | setAmex(?AmexInfo1 amex): void |
| `applePay` | [`?ApplePayInfo1`](../../doc/models/apple-pay-info-1.md) | Optional | Details to provide if `type` is **applepay**. | getApplePay(): ?ApplePayInfo1 | setApplePay(?ApplePayInfo1 applePay): void |
| `bcmc` | [`?BcmcInfo1`](../../doc/models/bcmc-info-1.md) | Optional | Details to provide if `type` is **bcmc** (Bancontact). | getBcmc(): ?BcmcInfo1 | setBcmc(?BcmcInfo1 bcmc): void |
| `businessLineId` | `?string` | Optional | The unique identifier of the business line. Required if you are a [platform model](https://docs.adyen.com/platforms). | getBusinessLineId(): ?string | setBusinessLineId(?string businessLineId): void |
| `cartesBancaires` | [`?CartesBancairesInfo1`](../../doc/models/cartes-bancaires-info-1.md) | Optional | Details to provide if `type` is **cartebancaire**. | getCartesBancaires(): ?CartesBancairesInfo1 | setCartesBancaires(?CartesBancairesInfo1 cartesBancaires): void |
| `clearpay` | [`?ClearpayInfo1`](../../doc/models/clearpay-info-1.md) | Optional | Details to provide if `type` is **clearpay**. | getClearpay(): ?ClearpayInfo1 | setClearpay(?ClearpayInfo1 clearpay): void |
| `countries` | `?(string[])` | Optional | The list of countries where a payment method is available. By default, all countries supported by the payment method. | getCountries(): ?array | setCountries(?array countries): void |
| `cup` | [`?GenericPmWithTdiInfo1`](../../doc/models/generic-pm-with-tdi-info-1.md) | Optional | Details to provide if `type` is **cup** (China Union Pay). | getCup(): ?GenericPmWithTdiInfo1 | setCup(?GenericPmWithTdiInfo1 cup): void |
| `currencies` | `?(string[])` | Optional | The list of currencies that a payment method supports. By default, all currencies supported by the payment method. | getCurrencies(): ?array | setCurrencies(?array currencies): void |
| `customRoutingFlags` | `?(string[])` | Optional | The list of custom routing flags to route payment to the intended acquirer. | getCustomRoutingFlags(): ?array | setCustomRoutingFlags(?array customRoutingFlags): void |
| `diners` | [`?DinersInfo1`](../../doc/models/diners-info-1.md) | Optional | Details to provide if `type` is **diners**.<br>For merchants operating in Japan, Diners payments are processed through the JCB network. This means that you must include [JCB-specific fields](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-jcb) in this object. | getDiners(): ?DinersInfo1 | setDiners(?DinersInfo1 diners): void |
| `discover` | [`?GenericPmWithTdiInfo2`](../../doc/models/generic-pm-with-tdi-info-2.md) | Optional | Details to provide if `type` is **discover**.<br>For merchants operating in Japan, request [Diners](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-diners) payment method instead. Discover is automatically requested, together with Diners. | getDiscover(): ?GenericPmWithTdiInfo2 | setDiscover(?GenericPmWithTdiInfo2 discover): void |
| `eftDirectdebitCa` | [`?GenericPmWithTdiInfo3`](../../doc/models/generic-pm-with-tdi-info-3.md) | Optional | Details to provide if `type` is **eft_directdebit_CA** (EFT PAD). | getEftDirectdebitCa(): ?GenericPmWithTdiInfo3 | setEftDirectdebitCa(?GenericPmWithTdiInfo3 eftDirectdebitCa): void |
| `eftposAustralia` | [`?GenericPmWithTdiInfo4`](../../doc/models/generic-pm-with-tdi-info-4.md) | Optional | Details to provide if `type` is **eftpos_australia**. | getEftposAustralia(): ?GenericPmWithTdiInfo4 | setEftposAustralia(?GenericPmWithTdiInfo4 eftposAustralia): void |
| `enabled` | `?bool` | Optional | Indicates whether the payment method is enabled (**true**) or disabled (**false**). | getEnabled(): ?bool | setEnabled(?bool enabled): void |
| `girocard` | [`?GenericPmWithTdiInfo5`](../../doc/models/generic-pm-with-tdi-info-5.md) | Optional | Details to provide if `type` is **girocard**. | getGirocard(): ?GenericPmWithTdiInfo5 | setGirocard(?GenericPmWithTdiInfo5 girocard): void |
| `givex` | [`?GivexInfo1`](../../doc/models/givex-info-1.md) | Optional | Details to provide if `type` is **givex**. | getGivex(): ?GivexInfo1 | setGivex(?GivexInfo1 givex): void |
| `googlePay` | [`?GooglePayInfo1`](../../doc/models/google-pay-info-1.md) | Optional | Details to provide if `type` is **googlepay**. | getGooglePay(): ?GooglePayInfo1 | setGooglePay(?GooglePayInfo1 googlePay): void |
| `id` | `string` | Required | The identifier of the resource. | getId(): string | setId(string id): void |
| `ideal` | [`?GenericPmWithTdiInfo6`](../../doc/models/generic-pm-with-tdi-info-6.md) | Optional | Details to provide if `type` is **ideal**. | getIdeal(): ?GenericPmWithTdiInfo6 | setIdeal(?GenericPmWithTdiInfo6 ideal): void |
| `interacCard` | [`?GenericPmWithTdiInfo7`](../../doc/models/generic-pm-with-tdi-info-7.md) | Optional | Details to provide if `type` is **interac_card**. | getInteracCard(): ?GenericPmWithTdiInfo7 | setInteracCard(?GenericPmWithTdiInfo7 interacCard): void |
| `jcb` | [`?JcbInfo1`](../../doc/models/jcb-info-1.md) | Optional | Details to provide if `type` is **jcb**.<br>For merchants operating in Japan, `midNumber`, `reuseMidNumber`, and `serviceLevel` fields are required.<br>For merchants operating outside of Japan, these fields are not required. | getJcb(): ?JcbInfo1 | setJcb(?JcbInfo1 jcb): void |
| `klarna` | [`?KlarnaInfo1`](../../doc/models/klarna-info-1.md) | Optional | Details to provide if `type` is **klarna** or its variant.<br><br>You can use the following payment method `type` values for Klarna:<br><br>* **klarna**: Klarna Pay Later<br>* **klarna_account**: Klarna Pay over time<br>* **klarna_paynow**: Klarna Pay now<br>* **klarna_b2b**: [Billie via Klarna](https://docs.adyen.com/payment-methods/klarna/billie) | getKlarna(): ?KlarnaInfo1 | setKlarna(?KlarnaInfo1 klarna): void |
| `maestro` | [`?GenericPmWithTdiInfo8`](../../doc/models/generic-pm-with-tdi-info-8.md) | Optional | Details to provide if `type` is **maestro**.<br>In the US, `maestro` is not supported; use `maestro_usa` instead. | getMaestro(): ?GenericPmWithTdiInfo8 | setMaestro(?GenericPmWithTdiInfo8 maestro): void |
| `maestroUsa` | [`?GenericPmWithTdiInfo9`](../../doc/models/generic-pm-with-tdi-info-9.md) | Optional | Details to provide if `type` is **maestro_usa**.<br>Only for Maestro USA, otherwise use `maestro`. | getMaestroUsa(): ?GenericPmWithTdiInfo9 | setMaestroUsa(?GenericPmWithTdiInfo9 maestroUsa): void |
| `mc` | [`?GenericPmWithTdiInfo10`](../../doc/models/generic-pm-with-tdi-info-10.md) | Optional | Details to provide if `type` is **mc**. | getMc(): ?GenericPmWithTdiInfo10 | setMc(?GenericPmWithTdiInfo10 mc): void |
| `mealVoucherFr` | [`?MealVoucherFrInfo1`](../../doc/models/meal-voucher-fr-info-1.md) | Optional | Details to provide if `type` is **mealVoucher_FR**. | getMealVoucherFr(): ?MealVoucherFrInfo1 | setMealVoucherFr(?MealVoucherFrInfo1 mealVoucherFr): void |
| `nyce` | [`?NyceInfo1`](../../doc/models/nyce-info-1.md) | Optional | Details to provide if `type` is **nyce**. | getNyce(): ?NyceInfo1 | setNyce(?NyceInfo1 nyce): void |
| `paybybankPlaid` | [`?PayByBankPlaidInfo1`](../../doc/models/pay-by-bank-plaid-info-1.md) | Optional | Details to provide if `type` is **paybybank_plaid**. | getPaybybankPlaid(): ?PayByBankPlaidInfo1 | setPaybybankPlaid(?PayByBankPlaidInfo1 paybybankPlaid): void |
| `payme` | [`?PayMeInfo1`](../../doc/models/pay-me-info-1.md) | Optional | Details to provide if `type` is **payme**. | getPayme(): ?PayMeInfo1 | setPayme(?PayMeInfo1 payme): void |
| `paypal` | [`?PayPalInfo1`](../../doc/models/pay-pal-info-1.md) | Optional | Details to provide if `type` is **paypal**. | getPaypal(): ?PayPalInfo1 | setPaypal(?PayPalInfo1 paypal): void |
| `payto` | [`?PayToInfo1`](../../doc/models/pay-to-info-1.md) | Optional | Details to provide if `type` is **payto**. | getPayto(): ?PayToInfo1 | setPayto(?PayToInfo1 payto): void |
| `pulse` | [`?PulseInfo1`](../../doc/models/pulse-info-1.md) | Optional | Details to provide if `type` is **pulse**. | getPulse(): ?PulseInfo1 | setPulse(?PulseInfo1 pulse): void |
| `reference` | `?string` | Optional | Your reference for the payment method. Supported characters a-z, A-Z, 0-9.<br><br>**Constraints**: *Maximum Length*: `150` | getReference(): ?string | setReference(?string reference): void |
| `sepadirectdebit` | [`?SepaDirectDebitInfo1`](../../doc/models/sepa-direct-debit-info-1.md) | Optional | Details to provide if `type` is **sepadirectdebit**. | getSepadirectdebit(): ?SepaDirectDebitInfo1 | setSepadirectdebit(?SepaDirectDebitInfo1 sepadirectdebit): void |
| `shopperInteraction` | `?string` | Optional | The sales channel. | getShopperInteraction(): ?string | setShopperInteraction(?string shopperInteraction): void |
| `sodexo` | [`?SodexoInfo1`](../../doc/models/sodexo-info-1.md) | Optional | Details to provide if `type` is **sodexo**. | getSodexo(): ?SodexoInfo1 | setSodexo(?SodexoInfo1 sodexo): void |
| `sofort` | [`?SofortInfo1`](../../doc/models/sofort-info-1.md) | Optional | Sofort details. | getSofort(): ?SofortInfo1 | setSofort(?SofortInfo1 sofort): void |
| `star` | [`?StarInfo1`](../../doc/models/star-info-1.md) | Optional | Details to provide if `type` is **star**. | getStar(): ?StarInfo1 | setStar(?StarInfo1 star): void |
| `storeIds` | `?(string[])` | Optional | The unique identifier of the store for which to configure the payment method, if any. | getStoreIds(): ?array | setStoreIds(?array storeIds): void |
| `svs` | [`?SvsInfo1`](../../doc/models/svs-info-1.md) | Optional | Details to provide if `type` is **svs**. | getSvs(): ?SvsInfo1 | setSvs(?SvsInfo1 svs): void |
| `swish` | [`?SwishInfo1`](../../doc/models/swish-info-1.md) | Optional | Details to provide if `type` is **swish**.<br><br>- This field is required only if you have a contract with Swish. Swish handles settlement directly with you (not through Adyen).<br>- If not specified then it's assumed that you are using Adyen's contract with Swish.You don't have a direct relationship with Swish. | getSwish(): ?SwishInfo1 | setSwish(?SwishInfo1 swish): void |
| `ticket` | [`?TicketInfo1`](../../doc/models/ticket-info-1.md) | Optional | Details to provide if `type` is **ticket** (Edenred Brazil). | getTicket(): ?TicketInfo1 | setTicket(?TicketInfo1 ticket): void |
| `twint` | [`?TwintInfo1`](../../doc/models/twint-info-1.md) | Optional | Details to provide if `type` is **twint**. | getTwint(): ?TwintInfo1 | setTwint(?TwintInfo1 twint): void |
| `type` | `?string` | Optional | Payment method [variant](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api). | getType(): ?string | setType(?string type): void |
| `valuelink` | [`?ValuelinkInfo1`](../../doc/models/valuelink-info-1.md) | Optional | Details to provide if `type` is **valuelink**. | getValuelink(): ?ValuelinkInfo1 | setValuelink(?ValuelinkInfo1 valuelink): void |
| `verificationStatus` | [`?string(VerificationStatus)`](../../doc/models/verification-status.md) | Optional | Payment method status. Possible values:<br><br>* **valid**<br>* **pending**<br>* **invalid**<br>* **rejected** | getVerificationStatus(): ?string | setVerificationStatus(?string verificationStatus): void |
| `vipps` | [`?VippsInfo1`](../../doc/models/vipps-info-1.md) | Optional | Details to provide if `type` is **vipps**. | getVipps(): ?VippsInfo1 | setVipps(?VippsInfo1 vipps): void |
| `visa` | [`?GenericPmWithTdiInfo11`](../../doc/models/generic-pm-with-tdi-info-11.md) | Optional | Details to provide if `type` is **visa**. | getVisa(): ?GenericPmWithTdiInfo11 | setVisa(?GenericPmWithTdiInfo11 visa): void |
| `wechatpay` | [`?WeChatPayInfo1`](../../doc/models/we-chat-pay-info-1.md) | Optional | Details to provide if `type` is **wechatpay**. | getWechatpay(): ?WeChatPayInfo1 | setWechatpay(?WeChatPayInfo1 wechatpay): void |
| `wechatpayPos` | [`?WeChatPayPosInfo1`](../../doc/models/we-chat-pay-pos-info-1.md) | Optional | Details to provide if `type` is **wechatpay_pos**. | getWechatpayPos(): ?WeChatPayPosInfo1 | setWechatpayPos(?WeChatPayPosInfo1 wechatpayPos): void |

## Example (as JSON)

```json
{
  "accel": {
    "processingType": "billpay",
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  },
  "affirm": {
    "pricePlan": "BRONZE",
    "supportEmail": "supportEmail2"
  },
  "afterpayTouch": {
    "supportEmail": "supportEmail8",
    "supportUrl": "supportUrl4"
  },
  "alipayPlus": {
    "settlementCurrencyCode": "settlementCurrencyCode0"
  },
  "allowed": false,
  "id": "id2"
}
```

