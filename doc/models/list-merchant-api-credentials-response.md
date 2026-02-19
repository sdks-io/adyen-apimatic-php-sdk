
# List Merchant Api Credentials Response

## Structure

`ListMerchantApiCredentialsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. | getLinks(): ?PaginationLinks1 | setLinks(?PaginationLinks1 links): void |
| `data` | [`?(ApiCredential[])`](../../doc/models/api-credential.md) | Optional | The list of API credentials. | getData(): ?array | setData(?array data): void |
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
        "allowedOrigins": {
          "href": "href6"
        },
        "company": {
          "href": "href2"
        },
        "generateApiKey": {
          "href": "href6"
        },
        "generateClientKey": {
          "href": "href4"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        }
      },
      "active": false,
      "allowedIpAddresses": [
        "allowedIpAddresses5"
      ],
      "allowedOrigins": [
        {
          "_links": {
            "self": {
              "href": "href0"
            }
          },
          "domain": "domain0",
          "id": "id4"
        }
      ],
      "clientKey": "clientKey6",
      "description": "description0",
      "id": "id0",
      "roles": [
        "roles8"
      ],
      "username": "username0"
    },
    {
      "_links": {
        "allowedOrigins": {
          "href": "href6"
        },
        "company": {
          "href": "href2"
        },
        "generateApiKey": {
          "href": "href6"
        },
        "generateClientKey": {
          "href": "href4"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        }
      },
      "active": false,
      "allowedIpAddresses": [
        "allowedIpAddresses5"
      ],
      "allowedOrigins": [
        {
          "_links": {
            "self": {
              "href": "href0"
            }
          },
          "domain": "domain0",
          "id": "id4"
        }
      ],
      "clientKey": "clientKey6",
      "description": "description0",
      "id": "id0",
      "roles": [
        "roles8"
      ],
      "username": "username0"
    },
    {
      "_links": {
        "allowedOrigins": {
          "href": "href6"
        },
        "company": {
          "href": "href2"
        },
        "generateApiKey": {
          "href": "href6"
        },
        "generateClientKey": {
          "href": "href4"
        },
        "merchant": {
          "href": "href6"
        },
        "self": {
          "href": "href0"
        }
      },
      "active": false,
      "allowedIpAddresses": [
        "allowedIpAddresses5"
      ],
      "allowedOrigins": [
        {
          "_links": {
            "self": {
              "href": "href0"
            }
          },
          "domain": "domain0",
          "id": "id4"
        }
      ],
      "clientKey": "clientKey6",
      "description": "description0",
      "id": "id0",
      "roles": [
        "roles8"
      ],
      "username": "username0"
    }
  ],
  "itemsTotal": 214,
  "pagesTotal": 80
}
```

