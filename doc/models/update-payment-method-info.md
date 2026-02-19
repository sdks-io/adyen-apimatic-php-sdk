
# Update Payment Method Info

## Structure

`UpdatePaymentMethodInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accel` | [`?AccelInfo1`](../../doc/models/accel-info-1.md) | Optional | Details to provide if `type` is **accel**. | getAccel(): ?AccelInfo1 | setAccel(?AccelInfo1 accel): void |
| `bcmc` | [`?BcmcInfo1`](../../doc/models/bcmc-info-1.md) | Optional | Details to provide if `type` is **bcmc** (Bancontact). | getBcmc(): ?BcmcInfo1 | setBcmc(?BcmcInfo1 bcmc): void |
| `cartesBancaires` | [`?CartesBancairesInfo1`](../../doc/models/cartes-bancaires-info-1.md) | Optional | Details to provide if `type` is **cartebancaire**. | getCartesBancaires(): ?CartesBancairesInfo1 | setCartesBancaires(?CartesBancairesInfo1 cartesBancaires): void |
| `countries` | `?(string[])` | Optional | The list of countries where a payment method is available. By default, all countries supported by the payment method. | getCountries(): ?array | setCountries(?array countries): void |
| `cup` | [`?GenericPmWithTdiInfo1`](../../doc/models/generic-pm-with-tdi-info-1.md) | Optional | Details to provide if `type` is **cup** (China Union Pay). | getCup(): ?GenericPmWithTdiInfo1 | setCup(?GenericPmWithTdiInfo1 cup): void |
| `currencies` | `?(string[])` | Optional | The list of currencies that a payment method supports. By default, all currencies supported by the payment method. | getCurrencies(): ?array | setCurrencies(?array currencies): void |
| `customRoutingFlags` | `?(string[])` | Optional | Custom routing flags for acquirer routing. | getCustomRoutingFlags(): ?array | setCustomRoutingFlags(?array customRoutingFlags): void |
| `diners` | [`?GenericPmWithTdiInfo24`](../../doc/models/generic-pm-with-tdi-info-24.md) | Optional | Details to provide if `type` is **diners**.<br>For merchants operating in Japan, Diners payments are processed through the JCB network. This means that you must include [JCB-specific fields](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-jcb) in this object. | getDiners(): ?GenericPmWithTdiInfo24 | setDiners(?GenericPmWithTdiInfo24 diners): void |
| `discover` | [`?GenericPmWithTdiInfo2`](../../doc/models/generic-pm-with-tdi-info-2.md) | Optional | Details to provide if `type` is **discover**.<br>For merchants operating in Japan, request [Diners](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/(merchantId)/paymentMethodSettings/(paymentMethodId)#request-diners) payment method instead. Discover is automatically requested, together with Diners. | getDiscover(): ?GenericPmWithTdiInfo2 | setDiscover(?GenericPmWithTdiInfo2 discover): void |
| `eftDirectdebitCa` | [`?GenericPmWithTdiInfo3`](../../doc/models/generic-pm-with-tdi-info-3.md) | Optional | Details to provide if `type` is **eft_directdebit_CA** (EFT PAD). | getEftDirectdebitCa(): ?GenericPmWithTdiInfo3 | setEftDirectdebitCa(?GenericPmWithTdiInfo3 eftDirectdebitCa): void |
| `eftposAustralia` | [`?GenericPmWithTdiInfo4`](../../doc/models/generic-pm-with-tdi-info-4.md) | Optional | Details to provide if `type` is **eftpos_australia**. | getEftposAustralia(): ?GenericPmWithTdiInfo4 | setEftposAustralia(?GenericPmWithTdiInfo4 eftposAustralia): void |
| `enabled` | `?bool` | Optional | Indicates whether the payment method is enabled (**true**) or disabled (**false**). | getEnabled(): ?bool | setEnabled(?bool enabled): void |
| `girocard` | [`?GenericPmWithTdiInfo5`](../../doc/models/generic-pm-with-tdi-info-5.md) | Optional | Details to provide if `type` is **girocard**. | getGirocard(): ?GenericPmWithTdiInfo5 | setGirocard(?GenericPmWithTdiInfo5 girocard): void |
| `ideal` | [`?GenericPmWithTdiInfo6`](../../doc/models/generic-pm-with-tdi-info-6.md) | Optional | Details to provide if `type` is **ideal**. | getIdeal(): ?GenericPmWithTdiInfo6 | setIdeal(?GenericPmWithTdiInfo6 ideal): void |
| `interacCard` | [`?GenericPmWithTdiInfo7`](../../doc/models/generic-pm-with-tdi-info-7.md) | Optional | Details to provide if `type` is **interac_card**. | getInteracCard(): ?GenericPmWithTdiInfo7 | setInteracCard(?GenericPmWithTdiInfo7 interacCard): void |
| `jcb` | [`?GenericPmWithTdiInfo31`](../../doc/models/generic-pm-with-tdi-info-31.md) | Optional | Details to provide if `type` is **jcb**.<br>For merchants operating in Japan, `midNumber`, `reuseMidNumber`, and `serviceLevel` fields are required.<br>For merchants operating outside of Japan, these fields are not required. | getJcb(): ?GenericPmWithTdiInfo31 | setJcb(?GenericPmWithTdiInfo31 jcb): void |
| `maestro` | [`?GenericPmWithTdiInfo8`](../../doc/models/generic-pm-with-tdi-info-8.md) | Optional | Details to provide if `type` is **maestro**.<br>In the US, `maestro` is not supported; use `maestro_usa` instead. | getMaestro(): ?GenericPmWithTdiInfo8 | setMaestro(?GenericPmWithTdiInfo8 maestro): void |
| `maestroUsa` | [`?GenericPmWithTdiInfo9`](../../doc/models/generic-pm-with-tdi-info-9.md) | Optional | Details to provide if `type` is **maestro_usa**.<br>Only for Maestro USA, otherwise use `maestro`. | getMaestroUsa(): ?GenericPmWithTdiInfo9 | setMaestroUsa(?GenericPmWithTdiInfo9 maestroUsa): void |
| `mc` | [`?GenericPmWithTdiInfo10`](../../doc/models/generic-pm-with-tdi-info-10.md) | Optional | Details to provide if `type` is **mc**. | getMc(): ?GenericPmWithTdiInfo10 | setMc(?GenericPmWithTdiInfo10 mc): void |
| `nyce` | [`?NyceInfo1`](../../doc/models/nyce-info-1.md) | Optional | Details to provide if `type` is **nyce**. | getNyce(): ?NyceInfo1 | setNyce(?NyceInfo1 nyce): void |
| `paybybankPlaid` | [`?PayByBankPlaidInfo1`](../../doc/models/pay-by-bank-plaid-info-1.md) | Optional | Details to provide if `type` is **paybybank_plaid**. | getPaybybankPlaid(): ?PayByBankPlaidInfo1 | setPaybybankPlaid(?PayByBankPlaidInfo1 paybybankPlaid): void |
| `pulse` | [`?PulseInfo1`](../../doc/models/pulse-info-1.md) | Optional | Details to provide if `type` is **pulse**. | getPulse(): ?PulseInfo1 | setPulse(?PulseInfo1 pulse): void |
| `sepadirectdebit` | [`?SepaDirectDebitInfo1`](../../doc/models/sepa-direct-debit-info-1.md) | Optional | Details to provide if `type` is **sepadirectdebit**. | getSepadirectdebit(): ?SepaDirectDebitInfo1 | setSepadirectdebit(?SepaDirectDebitInfo1 sepadirectdebit): void |
| `star` | [`?StarInfo1`](../../doc/models/star-info-1.md) | Optional | Details to provide if `type` is **star**. | getStar(): ?StarInfo1 | setStar(?StarInfo1 star): void |
| `storeId` | `?string` | Optional | The store for this payment method | getStoreId(): ?string | setStoreId(?string storeId): void |
| `storeIds` | `?(string[])` | Optional | The list of stores for this payment method | getStoreIds(): ?array | setStoreIds(?array storeIds): void |
| `visa` | [`?GenericPmWithTdiInfo11`](../../doc/models/generic-pm-with-tdi-info-11.md) | Optional | Details to provide if `type` is **visa**. | getVisa(): ?GenericPmWithTdiInfo11 | setVisa(?GenericPmWithTdiInfo11 visa): void |

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
  "bcmc": {
    "enableBcmcMobile": false
  },
  "cartesBancaires": {
    "siret": "siret8",
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  },
  "countries": [
    "countries3",
    "countries2",
    "countries1"
  ],
  "cup": {
    "transactionDescription": {
      "doingBusinessAsName": "doingBusinessAsName0",
      "type": "fixed"
    }
  }
}
```

