
# Pagination Links

## Structure

`PaginationLinks`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `first` | [`LinksElement9`](../../doc/models/links-element-9.md) | Required | The first page. | getFirst(): LinksElement9 | setFirst(LinksElement9 first): void |
| `last` | [`LinksElement10`](../../doc/models/links-element-10.md) | Required | The last page. | getLast(): LinksElement10 | setLast(LinksElement10 last): void |
| `next` | [`?LinksElement11`](../../doc/models/links-element-11.md) | Optional | The next page. Only present if there is a next page. | getNext(): ?LinksElement11 | setNext(?LinksElement11 next): void |
| `prev` | [`?LinksElement12`](../../doc/models/links-element-12.md) | Optional | The previous page. Only present if there is a previous page. | getPrev(): ?LinksElement12 | setPrev(?LinksElement12 prev): void |
| `self` | [`LinksElement13`](../../doc/models/links-element-13.md) | Required | The current page. | getSelf(): LinksElement13 | setSelf(LinksElement13 self): void |

## Example (as JSON)

```json
{
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
}
```

