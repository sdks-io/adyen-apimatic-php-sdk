
# Checkout Forward Response From Url

## Structure

`CheckoutForwardResponseFromUrl`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `body` | `?string` | Optional | The body of the response Adyen received from the third party, in string format. | getBody(): ?string | setBody(?string body): void |
| `headers` | `?array<string,string>` | Optional | The HTTP headers of the response Adyen received from the third party. | getHeaders(): ?array | setHeaders(?array headers): void |
| `status` | `?int` | Optional | The HTTP status of the response Adyen received from the third party. | getStatus(): ?int | setStatus(?int status): void |

## Example (as JSON)

```json
{
  "body": "body0",
  "headers": {
    "key0": "headers7",
    "key1": "headers8",
    "key2": "headers9"
  },
  "status": 152
}
```

