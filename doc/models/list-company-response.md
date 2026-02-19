
# List Company Response

## Structure

`ListCompanyResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. | getLinks(): ?PaginationLinks1 | setLinks(?PaginationLinks1 links): void |
| `data` | [`?(Company2[])`](../../doc/models/company-2.md) | Optional | The list of companies. | getData(): ?array | setData(?array data): void |
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
      "description": "description0",
      "id": "id0",
      "name": "name0"
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
      "description": "description0",
      "id": "id0",
      "name": "name0"
    }
  ],
  "itemsTotal": 112,
  "pagesTotal": 182
}
```

