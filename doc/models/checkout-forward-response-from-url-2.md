
# Checkout Forward Response From Url 2

The details of the response Adyen received from the third party.

## Structure

`CheckoutForwardResponseFromUrl2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `body` | `?string` | Optional | The body of the response Adyen received from the third party, in string format. | getBody(): ?string | setBody(?string body): void |
| `headers` | `?array<string,string>` | Optional | The HTTP headers of the response Adyen received from the third party. | getHeaders(): ?array | setHeaders(?array headers): void |
| `status` | `?int` | Optional | The HTTP status of the response Adyen received from the third party. | getStatus(): ?int | setStatus(?int status): void |

## Example (as JSON)

```json
{
  "body": "body8",
  "headers": {
    "key0": "headers5",
    "key1": "headers6",
    "key2": "headers7"
  },
  "status": 2
}
```

