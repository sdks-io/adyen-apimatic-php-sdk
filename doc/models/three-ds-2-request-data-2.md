
# Three Ds 2 Request Data 2

Request fields for 3D Secure 2. To check if any of the following fields are required for your integration, refer to [Online payments](https://docs.adyen.com/online-payments) or [Classic integration](https://docs.adyen.com/classic-integration) documentation.

## Structure

`ThreeDs2RequestData2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `acctInfo` | [`?AcctInfo1`](../../doc/models/acct-info-1.md) | Optional | Additional information about the cardholder’s account provided by the 3DS Requestor. | getAcctInfo(): ?AcctInfo1 | setAcctInfo(?AcctInfo1 acctInfo): void |
| `acctType` | [`?string(AcctType)`](../../doc/models/acct-type.md) | Optional | Indicates the type of account. For example, for a multi-account card product. Length: 2 characters. Allowed values:<br><br>* **01** — Not applicable<br>* **02** — Credit<br>* **03** — Debit<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` | getAcctType(): ?string | setAcctType(?string acctType): void |
| `acquirerBin` | `?string` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The acquiring BIN enrolled for 3D Secure 2. This string should match the value that you will use in the authorisation. Use 123456 on the Test platform. | getAcquirerBin(): ?string | setAcquirerBin(?string acquirerBin): void |
| `acquirerMerchantId` | `?string` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The merchantId that is enrolled for 3D Secure 2 by the merchant's acquirer. This string should match the value that you will use in the authorisation. Use 123456 on the Test platform. | getAcquirerMerchantId(): ?string | setAcquirerMerchantId(?string acquirerMerchantId): void |
| `addrMatch` | [`?string(AddrMatch)`](../../doc/models/addr-match.md) | Optional | Indicates whether the cardholder shipping address and cardholder billing address are the same. Allowed values:<br><br>* **Y** — Shipping address matches billing address.<br>* **N** — Shipping address does not match billing address.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1` | getAddrMatch(): ?string | setAddrMatch(?string addrMatch): void |
| `authenticationOnly` | `?bool` | Optional | If set to true, you will only perform the [3D Secure 2 authentication](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only), and not the payment authorisation.<br><br>**Default**: `false` | getAuthenticationOnly(): ?bool | setAuthenticationOnly(?bool authenticationOnly): void |
| `challengeIndicator` | [`?string(ChallengeIndicator)`](../../doc/models/challenge-indicator.md) | Optional | Possibility to specify a preference for receiving a challenge from the issuer.<br>Allowed values:<br><br>* `noPreference`<br>* `requestNoChallenge`<br>* `requestChallenge`<br>* `requestChallengeAsMandate` | getChallengeIndicator(): ?string | setChallengeIndicator(?string challengeIndicator): void |
| `deviceChannel` | `string` | Required | The environment of the shopper.<br>Allowed values:<br><br>* `app`<br>* `browser` | getDeviceChannel(): string | setDeviceChannel(string deviceChannel): void |
| `deviceRenderOptions` | [`?DeviceRenderOptions2`](../../doc/models/device-render-options-2.md) | Optional | Display options for the 3D Secure 2 SDK.<br>Optional and only for `deviceChannel` **app**. | getDeviceRenderOptions(): ?DeviceRenderOptions2 | setDeviceRenderOptions(?DeviceRenderOptions2 deviceRenderOptions): void |
| `homePhone` | [`?Phone3`](../../doc/models/phone-3.md) | Optional | The home phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. | getHomePhone(): ?Phone3 | setHomePhone(?Phone3 homePhone): void |
| `mcc` | `?string` | Optional | Required for merchants that have been enrolled for 3D Secure 2 by another party than Adyen, mostly [authentication-only integrations](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The `mcc` is a four-digit code with which the previously given `acquirerMerchantID` is registered at the scheme. | getMcc(): ?string | setMcc(?string mcc): void |
| `merchantName` | `?string` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only). The merchant name that the issuer presents to the shopper if they get a challenge. We recommend to use the same value that you will use in the authorization. Maximum length is 40 characters.<br><br>> Optional for a [full 3D Secure 2 integration](https://docs.adyen.com/online-payments/3d-secure/native-3ds2/api-integration). Use this field if you are enrolled for 3D Secure 2 with us and want to override the merchant name already configured on your account. | getMerchantName(): ?string | setMerchantName(?string merchantName): void |
| `messageVersion` | `?string` | Optional | The `messageVersion` value indicating the 3D Secure 2 protocol version. | getMessageVersion(): ?string | setMessageVersion(?string messageVersion): void |
| `mobilePhone` | [`?Phone1`](../../doc/models/phone-1.md) | Optional | The mobile phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. | getMobilePhone(): ?Phone1 | setMobilePhone(?Phone1 mobilePhone): void |
| `notificationUrl` | `?string` | Optional | URL to where the issuer should send the `CRes`. Required if you are not using components for `channel` **Web** or if you are using classic integration `deviceChannel` **browser**. | getNotificationUrl(): ?string | setNotificationUrl(?string notificationUrl): void |
| `payTokenInd` | `?bool` | Optional | Value **true** indicates that the transaction was de-tokenised prior to being received by the ACS. | getPayTokenInd(): ?bool | setPayTokenInd(?bool payTokenInd): void |
| `paymentAuthenticationUseCase` | `?string` | Optional | Indicates the type of payment for which an authentication is requested (message extension) | getPaymentAuthenticationUseCase(): ?string | setPaymentAuthenticationUseCase(?string paymentAuthenticationUseCase): void |
| `purchaseInstalData` | `?string` | Optional | Indicates the maximum number of authorisations permitted for instalment payments. Length: 1–3 characters.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `3` | getPurchaseInstalData(): ?string | setPurchaseInstalData(?string purchaseInstalData): void |
| `recurringExpiry` | `?string` | Optional | Date after which no further authorisations shall be performed. Format: YYYYMMDD | getRecurringExpiry(): ?string | setRecurringExpiry(?string recurringExpiry): void |
| `recurringFrequency` | `?string` | Optional | Indicates the minimum number of days between authorisations. Maximum length: 4 characters.<br><br>**Constraints**: *Maximum Length*: `4` | getRecurringFrequency(): ?string | setRecurringFrequency(?string recurringFrequency): void |
| `sdkAppId` | `?string` | Optional | The `sdkAppID` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. | getSdkAppId(): ?string | setSdkAppId(?string sdkAppId): void |
| `sdkEncData` | `?string` | Optional | The `sdkEncData` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. | getSdkEncData(): ?string | setSdkEncData(?string sdkEncData): void |
| `sdkEphemPubKey` | [`?SdkEphemPubKey3`](../../doc/models/sdk-ephem-pub-key-3.md) | Optional | The `sdkEphemPubKey` value as received from the 3D Secure 2 SDK.<br>Required for `deviceChannel` set to **app**. | getSdkEphemPubKey(): ?SdkEphemPubKey3 | setSdkEphemPubKey(?SdkEphemPubKey3 sdkEphemPubKey): void |
| `sdkMaxTimeout` | `?int` | Optional | The maximum amount of time in minutes for the 3D Secure 2 authentication process.<br>Optional and only for `deviceChannel` set to **app**. Defaults to **60** minutes.<br><br>**Default**: `60` | getSdkMaxTimeout(): ?int | setSdkMaxTimeout(?int sdkMaxTimeout): void |
| `sdkReferenceNumber` | `?string` | Optional | The `sdkReferenceNumber` value as received from the 3D Secure 2 SDK.<br>Only for `deviceChannel` set to **app**. | getSdkReferenceNumber(): ?string | setSdkReferenceNumber(?string sdkReferenceNumber): void |
| `sdkTransId` | `?string` | Optional | The `sdkTransID` value as received from the 3D Secure 2 SDK.<br>Only for `deviceChannel` set to **app**. | getSdkTransId(): ?string | setSdkTransId(?string sdkTransId): void |
| `sdkVersion` | `?string` | Optional | Version of the 3D Secure 2 mobile SDK.<br>Only for `deviceChannel` set to **app**. | getSdkVersion(): ?string | setSdkVersion(?string sdkVersion): void |
| `threeDsCompInd` | `?string` | Optional | Completion indicator for the device fingerprinting. | getThreeDsCompInd(): ?string | setThreeDsCompInd(?string threeDsCompInd): void |
| `threeDsRequestorAuthenticationInd` | `?string` | Optional | Indicates the type of Authentication request. | getThreeDsRequestorAuthenticationInd(): ?string | setThreeDsRequestorAuthenticationInd(?string threeDsRequestorAuthenticationInd): void |
| `threeDsRequestorAuthenticationInfo` | [`?ThreeDsRequestorAuthenticationInfo1`](../../doc/models/three-ds-requestor-authentication-info-1.md) | Optional | Information about how the 3DS Requestor authenticated the cardholder before or during the transaction | getThreeDsRequestorAuthenticationInfo(): ?ThreeDsRequestorAuthenticationInfo1 | setThreeDsRequestorAuthenticationInfo(?ThreeDsRequestorAuthenticationInfo1 threeDsRequestorAuthenticationInfo): void |
| `threeDsRequestorChallengeInd` | [`?string(ThreeDsRequestorChallengeInd)`](../../doc/models/three-ds-requestor-challenge-ind.md) | Optional | Indicates whether a challenge is requested for this transaction. Possible values:<br><br>* **01** — No preference<br>* **02** — No challenge requested<br>* **03** — Challenge requested (3DS Requestor preference)<br>* **04** — Challenge requested (Mandate)<br>* **05** — No challenge (transactional risk analysis is already performed)<br>* **06** — Data Only | getThreeDsRequestorChallengeInd(): ?string | setThreeDsRequestorChallengeInd(?string threeDsRequestorChallengeInd): void |
| `threeDsRequestorId` | `?string` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only) for Visa. Unique 3D Secure requestor identifier assigned by the Directory Server when you enrol for 3D Secure 2. | getThreeDsRequestorId(): ?string | setThreeDsRequestorId(?string threeDsRequestorId): void |
| `threeDsRequestorName` | `?string` | Optional | Required for [authentication-only integration](https://docs.adyen.com/online-payments/3d-secure/other-3ds-flows/authentication-only) for Visa. Unique 3D Secure requestor name assigned by the Directory Server when you enrol for 3D Secure 2. | getThreeDsRequestorName(): ?string | setThreeDsRequestorName(?string threeDsRequestorName): void |
| `threeDsRequestorPriorAuthenticationInfo` | [`?ThreeDsRequestorPriorAuthenticationInfo1`](../../doc/models/three-ds-requestor-prior-authentication-info-1.md) | Optional | Information about how the 3DS Requestor authenticated the cardholder as part of a previous 3DS transaction. | getThreeDsRequestorPriorAuthenticationInfo(): ?ThreeDsRequestorPriorAuthenticationInfo1 | setThreeDsRequestorPriorAuthenticationInfo(?ThreeDsRequestorPriorAuthenticationInfo1 threeDsRequestorPriorAuthenticationInfo): void |
| `threeDsRequestorUrl` | `?string` | Optional | URL of the (customer service) website that will be shown to the shopper in case of technical errors during the 3D Secure 2 process. | getThreeDsRequestorUrl(): ?string | setThreeDsRequestorUrl(?string threeDsRequestorUrl): void |
| `transType` | [`?string(TransType)`](../../doc/models/trans-type.md) | Optional | Identifies the type of transaction being authenticated. Length: 2 characters. Allowed values:<br><br>* **01** — Goods/Service Purchase<br>* **03** — Check Acceptance<br>* **10** — Account Funding<br>* **11** — Quasi-Cash Transaction<br>* **28** — Prepaid Activation and Load<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` | getTransType(): ?string | setTransType(?string transType): void |
| `transactionType` | [`?string(TransactionType)`](../../doc/models/transaction-type.md) | Optional | Identify the type of the transaction being authenticated. | getTransactionType(): ?string | setTransactionType(?string transactionType): void |
| `whiteListStatus` | `?string` | Optional | The `whiteListStatus` value returned from a previous 3D Secure 2 transaction, only applicable for 3D Secure 2 protocol version 2.2.0. | getWhiteListStatus(): ?string | setWhiteListStatus(?string whiteListStatus): void |
| `workPhone` | [`?Phone2`](../../doc/models/phone-2.md) | Optional | The work phone number provided by the cardholder. The phone number must consist of a country code, followed by the number. If the value you provide does not follow the guidelines, we do not submit it for authentication.<br><br>> Required for Visa and JCB transactions that require 3D Secure 2 authentication, if you did not include the `shopperEmail`, and did not send the shopper's phone number in `telephoneNumber`. | getWorkPhone(): ?Phone2 | setWorkPhone(?Phone2 workPhone): void |

## Example (as JSON)

```json
{
  "authenticationOnly": false,
  "deviceChannel": "deviceChannel8",
  "sdkMaxTimeout": 60,
  "acctInfo": {
    "chAccAgeInd": "05",
    "chAccChange": "chAccChange8",
    "chAccChangeInd": "01",
    "chAccPwChange": "chAccPwChange8",
    "chAccPwChangeInd": "03"
  },
  "acctType": "03",
  "acquirerBIN": "acquirerBIN6",
  "acquirerMerchantID": "acquirerMerchantID4",
  "addrMatch": "Y"
}
```

