
# Payment Validations Name Response 2

Object that contains the status and outcomes of the [name validation](https://docs.adyen.com/payment-methods/cards/name-validation).

## Structure

`PaymentValidationsNameResponse2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rawResponse` | [`?PaymentValidationsNameResultRawResponse2`](../../doc/models/payment-validations-name-result-raw-response-2.md) | Optional | Contains the raw response(s) returned by the scheme for the name validation. | getRawResponse(): ?PaymentValidationsNameResultRawResponse2 | setRawResponse(?PaymentValidationsNameResultRawResponse2 rawResponse): void |
| `result` | [`?PaymentValidationsNameResultResponse2`](../../doc/models/payment-validations-name-result-response-2.md) | Optional | Contains the scheme-agnostic match values returned by Adyen. | getResult(): ?PaymentValidationsNameResultResponse2 | setResult(?PaymentValidationsNameResultResponse2 result): void |
| `status` | [`?string(Status)`](../../doc/models/status.md) | Optional | Informs you if the name validation was performed. Possible values:<br><br>**performed**, **notPerformed**, **notSupported** | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
{
  "rawResponse": {
    "firstName": "firstName0",
    "fullName": "fullName4",
    "lastName": "lastName8",
    "middleName": "middleName2",
    "status": "status6"
  },
  "result": {
    "firstName": "firstName8",
    "fullName": "fullName6",
    "lastName": "lastName0",
    "middleName": "middleName4"
  },
  "status": "notPerformed"
}
```

