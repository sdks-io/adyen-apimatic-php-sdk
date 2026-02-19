
# Company 2

## Structure

`Company2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?CompanyLinks2`](../../doc/models/company-links-2.md) | Optional | References to resources connected with this company. | getLinks(): ?CompanyLinks2 | setLinks(?CompanyLinks2 links): void |
| `dataCenters` | [`?(DataCenter[])`](../../doc/models/data-center.md) | Optional | List of available data centers.<br><br>Adyen has several data centers around the world.In the URL that you use for making API requests, we recommend you use the live URL prefix from the data center closest to your shoppers. | getDataCenters(): ?array | setDataCenters(?array dataCenters): void |
| `description` | `?string` | Optional | Your description for the company account, maximum 300 characters | getDescription(): ?string | setDescription(?string description): void |
| `id` | `?string` | Optional | The unique identifier of the company account. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The legal or trading name of the company. | getName(): ?string | setName(?string name): void |
| `reference` | `?string` | Optional | Your reference to the account | getReference(): ?string | setReference(?string reference): void |
| `status` | `?string` | Optional | The status of the company account.<br><br>Possible values:<br><br>* **Active**: Users can log in. Processing and payout capabilities depend on the status of the merchant account.<br>* **Inactive**: Users can log in. Payment processing and payouts are disabled.<br>* **Closed**: The company account is closed and this cannot be reversed. Users cannot log in. Payment processing and payouts are disabled. | getStatus(): ?string | setStatus(?string status): void |

## Example (as JSON)

```json
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
```

