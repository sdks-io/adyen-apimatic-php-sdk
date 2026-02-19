
# Event Url 2

The list of local and public URLs to send event notifications to when using Terminal API.

## Structure

`EventUrl2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `eventLocalUrls` | [`?(Url[])`](../../doc/models/url.md) | Optional | One or more local URLs to send event notifications to when using Terminal API. | getEventLocalUrls(): ?array | setEventLocalUrls(?array eventLocalUrls): void |
| `eventPublicUrls` | [`?(Url[])`](../../doc/models/url.md) | Optional | One or more public URLs to send event notifications to when using Terminal API. | getEventPublicUrls(): ?array | setEventPublicUrls(?array eventPublicUrls): void |

## Example (as JSON)

```json
{
  "eventLocalUrls": [
    {
      "encrypted": false,
      "password": "password4",
      "url": "url4",
      "username": "username0"
    },
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
    },
    {
      "encrypted": false,
      "password": "password8",
      "url": "url8",
      "username": "username4"
    }
  ]
}
```

