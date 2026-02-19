
# Three D Secure Data

## Structure

`ThreeDSecureData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `authenticationResponse` | [`?string(AuthenticationResponse)`](../../doc/models/authentication-response.md) | Optional | In 3D Secure 2, this is the `transStatus` from the challenge result. If the transaction was frictionless, omit this parameter. | getAuthenticationResponse(): ?string | setAuthenticationResponse(?string authenticationResponse): void |
| `cavv` | `?string` | Optional | The cardholder authentication value (base64 encoded, 20 bytes in a decoded form). | getCavv(): ?string | setCavv(?string cavv): void |
| `cavvAlgorithm` | `?string` | Optional | The CAVV algorithm used. Include this only for 3D Secure 1. | getCavvAlgorithm(): ?string | setCavvAlgorithm(?string cavvAlgorithm): void |
| `challengeCancel` | [`?string(ChallengeCancel)`](../../doc/models/challenge-cancel.md) | Optional | Indicator informing the Access Control Server (ACS) and the Directory Server (DS) that the authentication has been cancelled. For possible values, refer to [3D Secure API reference](https://docs.adyen.com/online-payments/3d-secure/api-reference#mpidata). | getChallengeCancel(): ?string | setChallengeCancel(?string challengeCancel): void |
| `directoryResponse` | [`?string(DirectoryResponse)`](../../doc/models/directory-response.md) | Optional | In 3D Secure 2, this is the `transStatus` from the `ARes`. | getDirectoryResponse(): ?string | setDirectoryResponse(?string directoryResponse): void |
| `dsTransId` | `?string` | Optional | Supported for 3D Secure 2. The unique transaction identifier assigned by the Directory Server (DS) to identify a single transaction. | getDsTransId(): ?string | setDsTransId(?string dsTransId): void |
| `eci` | `?string` | Optional | The electronic commerce indicator. | getEci(): ?string | setEci(?string eci): void |
| `riskScore` | `?string` | Optional | Risk score calculated by Directory Server (DS). Required for Cartes Bancaires integrations. | getRiskScore(): ?string | setRiskScore(?string riskScore): void |
| `threeDsVersion` | `?string` | Optional | The version of the 3D Secure protocol. | getThreeDsVersion(): ?string | setThreeDsVersion(?string threeDsVersion): void |
| `tokenAuthenticationVerificationValue` | `?string` | Optional | Network token authentication verification value (TAVV). The network token cryptogram. | getTokenAuthenticationVerificationValue(): ?string | setTokenAuthenticationVerificationValue(?string tokenAuthenticationVerificationValue): void |
| `transStatusReason` | `?string` | Optional | Provides information on why the `transStatus` field has the specified value. For possible values, refer to [our docs](https://docs.adyen.com/online-payments/3d-secure/api-reference#possible-transstatusreason-values). | getTransStatusReason(): ?string | setTransStatusReason(?string transStatusReason): void |
| `xid` | `?string` | Optional | Supported for 3D Secure 1. The transaction identifier (Base64-encoded, 20 bytes in a decoded form). | getXid(): ?string | setXid(?string xid): void |

## Example (as JSON)

```json
{
  "authenticationResponse": "Y",
  "cavv": "cavv6",
  "cavvAlgorithm": "cavvAlgorithm4",
  "challengeCancel": "02",
  "directoryResponse": "N"
}
```

