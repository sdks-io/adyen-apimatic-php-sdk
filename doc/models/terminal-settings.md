
# Terminal Settings

## Structure

`TerminalSettings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cardholderReceipt` | [`?CardholderReceipt1`](../../doc/models/cardholder-receipt-1.md) | Optional | Settings to define the header of the shopper receipt. | getCardholderReceipt(): ?CardholderReceipt1 | setCardholderReceipt(?CardholderReceipt1 cardholderReceipt): void |
| `connectivity` | [`?Connectivity1`](../../doc/models/connectivity-1.md) | Optional | Settings for terminal connectivity features. | getConnectivity(): ?Connectivity1 | setConnectivity(?Connectivity1 connectivity): void |
| `gratuities` | [`?(Gratuity[])`](../../doc/models/gratuity.md) | Optional | Settings for tipping with or without predefined options to choose from. The maximum number of predefined options is four, or three plus the option to enter a custom tip. | getGratuities(): ?array | setGratuities(?array gratuities): void |
| `hardware` | [`?Hardware1`](../../doc/models/hardware-1.md) | Optional | Settings for terminal hardware features. | getHardware(): ?Hardware1 | setHardware(?Hardware1 hardware): void |
| `homeScreen` | [`?HomeScreenSettings1`](../../doc/models/home-screen-settings-1.md) | Optional | Settings for the home screen. | getHomeScreen(): ?HomeScreenSettings1 | setHomeScreen(?HomeScreenSettings1 homeScreen): void |
| `kioskMode` | [`?KioskModeSettings1`](../../doc/models/kiosk-mode-settings-1.md) | Optional | Settings for kiosk mode. | getKioskMode(): ?KioskModeSettings1 | setKioskMode(?KioskModeSettings1 kioskMode): void |
| `localization` | [`?Localization1`](../../doc/models/localization-1.md) | Optional | Settings for localization. | getLocalization(): ?Localization1 | setLocalization(?Localization1 localization): void |
| `moto` | [`?Moto1`](../../doc/models/moto-1.md) | Optional | Settings for Mail Order/Telephone Order transactions. | getMoto(): ?Moto1 | setMoto(?Moto1 moto): void |
| `nexo` | [`?Nexo1`](../../doc/models/nexo-1.md) | Optional | Settings for a Terminal API integration. | getNexo(): ?Nexo1 | setNexo(?Nexo1 nexo): void |
| `offlineProcessing` | [`?OfflineProcessing1`](../../doc/models/offline-processing-1.md) | Optional | Settings for [offline payment](https://docs.adyen.com/point-of-sale/offline-payments) features. | getOfflineProcessing(): ?OfflineProcessing1 | setOfflineProcessing(?OfflineProcessing1 offlineProcessing): void |
| `opi` | [`?Opi1`](../../doc/models/opi-1.md) | Optional | Settings for an Oracle Payment Interface (OPI) integration. | getOpi(): ?Opi1 | setOpi(?Opi1 opi): void |
| `passcodes` | [`?Passcodes1`](../../doc/models/passcodes-1.md) | Optional | Settings for [passcodes](https://docs.adyen.com/point-of-sale/managing-terminals/menu-access?tab=manage_passcodes_with_an_api_call_2#manage-passcodes) features. | getPasscodes(): ?Passcodes1 | setPasscodes(?Passcodes1 passcodes): void |
| `payAtTable` | [`?PayAtTable1`](../../doc/models/pay-at-table-1.md) | Optional | Settings for [Pay-at-table](https://docs.adyen.com/point-of-sale/pay-at-x) features. | getPayAtTable(): ?PayAtTable1 | setPayAtTable(?PayAtTable1 payAtTable): void |
| `payment` | [`?Payment11`](../../doc/models/payment-11.md) | Optional | Settings for payment features. | getPayment(): ?Payment11 | setPayment(?Payment11 payment): void |
| `receiptOptions` | [`?ReceiptOptions1`](../../doc/models/receipt-options-1.md) | Optional | Generic receipt settings. | getReceiptOptions(): ?ReceiptOptions1 | setReceiptOptions(?ReceiptOptions1 receiptOptions): void |
| `receiptPrinting` | [`?ReceiptPrinting1`](../../doc/models/receipt-printing-1.md) | Optional | Transaction outcomes that you want the terminal to print a merchant receipt or a shopper receipt for. | getReceiptPrinting(): ?ReceiptPrinting1 | setReceiptPrinting(?ReceiptPrinting1 receiptPrinting): void |
| `refunds` | [`?Refunds1`](../../doc/models/refunds-1.md) | Optional | Settings for refunds. | getRefunds(): ?Refunds1 | setRefunds(?Refunds1 refunds): void |
| `signature` | [`?Signature1`](../../doc/models/signature-1.md) | Optional | Settings to skip signature, sign on display, or sign on receipt. | getSignature(): ?Signature1 | setSignature(?Signature1 signature): void |
| `standalone` | [`?Standalone1`](../../doc/models/standalone-1.md) | Optional | Settings for [standalone](https://docs.adyen.com/point-of-sale/standalone/standalone-build/set-up-standalone#set-up-standalone-using-an-api-call) features. | getStandalone(): ?Standalone1 | setStandalone(?Standalone1 standalone): void |
| `storeAndForward` | [`?StoreAndForward1`](../../doc/models/store-and-forward-1.md) | Optional | Settings for store-and-forward offline payments. The `maxAmount`, `maxPayments`, and `supportedCardTypes` parameters must be configured, either in the request or inherited from a higher level in your account structure. | getStoreAndForward(): ?StoreAndForward1 | setStoreAndForward(?StoreAndForward1 storeAndForward): void |
| `surcharge` | [`?Surcharge21`](../../doc/models/surcharge-21.md) | Optional | Settings for payment [surcharge](https://docs.adyen.com/point-of-sale/surcharge) features. | getSurcharge(): ?Surcharge21 | setSurcharge(?Surcharge21 surcharge): void |
| `tapToPay` | [`?TapToPay1`](../../doc/models/tap-to-pay-1.md) | Optional | Settings for Tap to Pay. | getTapToPay(): ?TapToPay1 | setTapToPay(?TapToPay1 tapToPay): void |
| `terminalInstructions` | [`?TerminalInstructions1`](../../doc/models/terminal-instructions-1.md) | Optional | Settings to define the behaviour of the payment terminal. | getTerminalInstructions(): ?TerminalInstructions1 | setTerminalInstructions(?TerminalInstructions1 terminalInstructions): void |
| `timeouts` | [`?Timeouts2`](../../doc/models/timeouts-2.md) | Optional | Settings for device [time-outs](https://docs.adyen.com/point-of-sale/pos-timeouts#device-time-out). | getTimeouts(): ?Timeouts2 | setTimeouts(?Timeouts2 timeouts): void |
| `wifiProfiles` | [`?WifiProfiles2`](../../doc/models/wifi-profiles-2.md) | Optional | Remote Wi-Fi profiles for WPA and WPA2 PSK and EAP Wi-Fi networks. | getWifiProfiles(): ?WifiProfiles2 | setWifiProfiles(?WifiProfiles2 wifiProfiles): void |

## Example (as JSON)

```json
{
  "cardholderReceipt": {
    "headerForAuthorizedReceipt": "headerForAuthorizedReceipt8"
  },
  "connectivity": {
    "simcardStatus": "ACTIVATED",
    "terminalIPAddressURL": {
      "eventLocalUrls": [
        {
          "encrypted": false,
          "password": "password4",
          "url": "url4",
          "username": "username0"
        }
      ],
      "eventPublicUrls": [
        {
          "encrypted": false,
          "password": "password8",
          "url": "url8",
          "username": "username4"
        },
        {
          "encrypted": false,
          "password": "password8",
          "url": "url8",
          "username": "username4"
        }
      ]
    }
  },
  "gratuities": [
    {
      "allowCustomAmount": false,
      "currency": "currency0",
      "predefinedTipEntries": [
        "predefinedTipEntries0",
        "predefinedTipEntries1",
        "predefinedTipEntries2"
      ],
      "usePredefinedTipEntries": false
    },
    {
      "allowCustomAmount": false,
      "currency": "currency0",
      "predefinedTipEntries": [
        "predefinedTipEntries0",
        "predefinedTipEntries1",
        "predefinedTipEntries2"
      ],
      "usePredefinedTipEntries": false
    },
    {
      "allowCustomAmount": false,
      "currency": "currency0",
      "predefinedTipEntries": [
        "predefinedTipEntries0",
        "predefinedTipEntries1",
        "predefinedTipEntries2"
      ],
      "usePredefinedTipEntries": false
    }
  ],
  "hardware": {
    "displayMaximumBackLight": 142,
    "resetTotalsHour": 132,
    "restartHour": 110
  },
  "homeScreen": {
    "hideNavigationBar": false,
    "showPaymentsMenu": false,
    "showSettingsMenu": false
  }
}
```

