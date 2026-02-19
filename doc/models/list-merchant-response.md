
# List Merchant Response

## Structure

`ListMerchantResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. | getLinks(): ?PaginationLinks1 | setLinks(?PaginationLinks1 links): void |
| `data` | [`?(Merchant[])`](../../doc/models/merchant.md) | Optional | The list of merchant accounts. | getData(): ?array | setData(?array data): void |
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
  "data": [
    {
      "_links": {
        "apiCredentials": {
          "href": "href8"
        },
        "self": {
          "href": "href0"
        },
        "users": {
          "href": "href8"
        },
        "webhooks": {
          "href": "href8"
        }
      },
      "captureDelay": "captureDelay6",
      "companyId": "companyId0",
      "dataCenters": [
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        }
      ],
      "defaultShopperInteraction": "defaultShopperInteraction8"
    },
    {
      "_links": {
        "apiCredentials": {
          "href": "href8"
        },
        "self": {
          "href": "href0"
        },
        "users": {
          "href": "href8"
        },
        "webhooks": {
          "href": "href8"
        }
      },
      "captureDelay": "captureDelay6",
      "companyId": "companyId0",
      "dataCenters": [
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        }
      ],
      "defaultShopperInteraction": "defaultShopperInteraction8"
    },
    {
      "_links": {
        "apiCredentials": {
          "href": "href8"
        },
        "self": {
          "href": "href0"
        },
        "users": {
          "href": "href8"
        },
        "webhooks": {
          "href": "href8"
        }
      },
      "captureDelay": "captureDelay6",
      "companyId": "companyId0",
      "dataCenters": [
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        },
        {
          "livePrefix": "livePrefix4",
          "name": "name6"
        }
      ],
      "defaultShopperInteraction": "defaultShopperInteraction8"
    }
  ],
  "itemsTotal": 66,
  "pagesTotal": 28
}
```

