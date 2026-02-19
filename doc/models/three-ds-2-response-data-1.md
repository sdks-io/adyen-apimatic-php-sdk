
# Three Ds 2 Response Data 1

Response of the 3D Secure 2 authentication.

## Structure

`ThreeDs2ResponseData1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `acsChallengeMandated` | `?string` | Optional | - | getAcsChallengeMandated(): ?string | setAcsChallengeMandated(?string acsChallengeMandated): void |
| `acsOperatorId` | `?string` | Optional | - | getAcsOperatorId(): ?string | setAcsOperatorId(?string acsOperatorId): void |
| `acsReferenceNumber` | `?string` | Optional | - | getAcsReferenceNumber(): ?string | setAcsReferenceNumber(?string acsReferenceNumber): void |
| `acsSignedContent` | `?string` | Optional | - | getAcsSignedContent(): ?string | setAcsSignedContent(?string acsSignedContent): void |
| `acsTransId` | `?string` | Optional | - | getAcsTransId(): ?string | setAcsTransId(?string acsTransId): void |
| `acsUrl` | `?string` | Optional | - | getAcsUrl(): ?string | setAcsUrl(?string acsUrl): void |
| `authenticationType` | `?string` | Optional | - | getAuthenticationType(): ?string | setAuthenticationType(?string authenticationType): void |
| `cardHolderInfo` | `?string` | Optional | - | getCardHolderInfo(): ?string | setCardHolderInfo(?string cardHolderInfo): void |
| `cavvAlgorithm` | `?string` | Optional | - | getCavvAlgorithm(): ?string | setCavvAlgorithm(?string cavvAlgorithm): void |
| `challengeIndicator` | `?string` | Optional | - | getChallengeIndicator(): ?string | setChallengeIndicator(?string challengeIndicator): void |
| `dsReferenceNumber` | `?string` | Optional | - | getDsReferenceNumber(): ?string | setDsReferenceNumber(?string dsReferenceNumber): void |
| `dsTransId` | `?string` | Optional | - | getDsTransId(): ?string | setDsTransId(?string dsTransId): void |
| `exemptionIndicator` | `?string` | Optional | - | getExemptionIndicator(): ?string | setExemptionIndicator(?string exemptionIndicator): void |
| `messageVersion` | `?string` | Optional | - | getMessageVersion(): ?string | setMessageVersion(?string messageVersion): void |
| `riskScore` | `?string` | Optional | - | getRiskScore(): ?string | setRiskScore(?string riskScore): void |
| `sdkEphemPubKey` | `?string` | Optional | - | getSdkEphemPubKey(): ?string | setSdkEphemPubKey(?string sdkEphemPubKey): void |
| `threeDsServerTransId` | `?string` | Optional | - | getThreeDsServerTransId(): ?string | setThreeDsServerTransId(?string threeDsServerTransId): void |
| `transStatus` | `?string` | Optional | - | getTransStatus(): ?string | setTransStatus(?string transStatus): void |
| `transStatusReason` | `?string` | Optional | - | getTransStatusReason(): ?string | setTransStatusReason(?string transStatusReason): void |

## Example (as JSON)

```json
{
  "acsChallengeMandated": "acsChallengeMandated0",
  "acsOperatorID": "acsOperatorID0",
  "acsReferenceNumber": "acsReferenceNumber0",
  "acsSignedContent": "acsSignedContent6",
  "acsTransID": "acsTransID0"
}
```

