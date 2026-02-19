
# List Merchant Users Response

## Structure

`ListMerchantUsersResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?PaginationLinks1`](../../doc/models/pagination-links-1.md) | Optional | Pagination references. | getLinks(): ?PaginationLinks1 | setLinks(?PaginationLinks1 links): void |
| `data` | [`?(User[])`](../../doc/models/user.md) | Optional | The list of users. | getData(): ?array | setData(?array data): void |
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
        "self": {
          "href": "href0"
        }
      },
      "accountGroups": [
        "accountGroups7"
      ],
      "active": false,
      "apps": [
        "apps4",
        "apps5",
        "apps6"
      ],
      "email": "email6",
      "id": "id0",
      "name": {
        "firstName": "firstName4",
        "lastName": "lastName4"
      },
      "roles": [
        "roles8"
      ],
      "timeZoneCode": "timeZoneCode2",
      "username": "username0"
    },
    {
      "_links": {
        "self": {
          "href": "href0"
        }
      },
      "accountGroups": [
        "accountGroups7"
      ],
      "active": false,
      "apps": [
        "apps4",
        "apps5",
        "apps6"
      ],
      "email": "email6",
      "id": "id0",
      "name": {
        "firstName": "firstName4",
        "lastName": "lastName4"
      },
      "roles": [
        "roles8"
      ],
      "timeZoneCode": "timeZoneCode2",
      "username": "username0"
    }
  ],
  "itemsTotal": 244,
  "pagesTotal": 206
}
```

