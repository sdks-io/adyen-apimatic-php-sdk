
# Response Additional Data 3 D Secure

## Structure

`ResponseAdditionalData3DSecure`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cardHolderInfo` | `?string` | Optional | Information provided by the issuer to the cardholder. If this field is present, you need to display this information to the cardholder. | getCardHolderInfo(): ?string | setCardHolderInfo(?string cardHolderInfo): void |
| `cavv` | `?string` | Optional | The Cardholder Authentication Verification Value (CAVV) for the 3D Secure authentication session, as a Base64-encoded 20-byte array. | getCavv(): ?string | setCavv(?string cavv): void |
| `cavvAlgorithm` | `?string` | Optional | The CAVV algorithm used. | getCavvAlgorithm(): ?string | setCavvAlgorithm(?string cavvAlgorithm): void |
| `scaExemptionRequested` | `?string` | Optional | Shows the [exemption type](https://docs.adyen.com/payments-fundamentals/psd2-sca-compliance-and-implementation-guide#specifypreferenceinyourapirequest) that Adyen requested for the payment.<br><br>Possible values:<br><br>* **lowValue**<br>* **secureCorporate**<br>* **trustedBeneficiary**<br>* **transactionRiskAnalysis** | getScaExemptionRequested(): ?string | setScaExemptionRequested(?string scaExemptionRequested): void |
| `threeds2CardEnrolled` | `?bool` | Optional | Indicates whether a card is enrolled for 3D Secure 2. | getThreeds2CardEnrolled(): ?bool | setThreeds2CardEnrolled(?bool threeds2CardEnrolled): void |

## Example (as JSON)

```json
{
  "cardHolderInfo": "cardHolderInfo6",
  "cavv": "cavv6",
  "cavvAlgorithm": "cavvAlgorithm4",
  "scaExemptionRequested": "scaExemptionRequested4",
  "threeds2.cardEnrolled": false
}
```

