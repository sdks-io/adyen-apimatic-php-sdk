
# List Webhooks Response

## Structure

`ListWebhooksResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. | getLinks(): ?PaginationLinks1 | setLinks(?PaginationLinks1 links): void |
| `accountReference` | `?string` | Optional | Reference to the account. | getAccountReference(): ?string | setAccountReference(?string accountReference): void |
| `data` | [`?(Webhook[])`](../../doc/models/webhook.md) | Optional | The list of webhooks configured for this account. | getData(): ?array | setData(?array data): void |
| `itemsTotal` | `int` | Required | Total number of items. | getItemsTotal(): int | setItemsTotal(int itemsTotal): void |
| `pagesTotal` | `int` | Required | Total number of pages. | getPagesTotal(): int | setPagesTotal(int pagesTotal): void |

## Example (as JSON)

```json
{
  "_links": {
    "first": {
      "href": "href2"
    },
    "last": {
      "href": "href2"
    },
    "next": {
      "href": "href4"
    },
    "prev": {
      "href": "href8"
    },
    "self": {
      "href": "href0"
    }
  },
  "accountReference": "accountReference2",
  "data": [
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    },
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    },
    {
      "_links": {
        "company": {
          "href": "href2"
        },
        "generateHmac": {
          "href": "href6"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        },
        "testWebhook": {
          "href": "href6"
        }
      },
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "accountReference": "accountReference2",
      "active": false,
      "communicationFormat": "json",
      "type": "type0",
      "url": "url4"
    }
  ],
  "itemsTotal": 90,
  "pagesTotal": 204
}
```

