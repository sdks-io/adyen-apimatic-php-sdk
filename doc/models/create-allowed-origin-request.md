
# Create Allowed Origin Request

## Structure

`CreateAllowedOriginRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?Links2`](../../doc/models/links-2.md) | Optional | References to resources linked to the allowed origin. | getLinks(): ?Links2 | setLinks(?Links2 links): void |
| `domain` | `string` | Required | Domain of the allowed origin. | getDomain(): string | setDomain(string domain): void |
| `id` | `?string` | Optional | Unique identifier of the allowed origin. | getId(): ?string | setId(?string id): void |

## Example (as JSON)

```json
{
  "domain": "https://adyen.com",
  "_links": {
    "self": {
      "href": "href0"
    }
  },
  "id": "id8"
}
```

