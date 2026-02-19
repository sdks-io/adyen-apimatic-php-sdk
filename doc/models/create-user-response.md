
# Create User Response

## Structure

`CreateUserResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `links` | [`?Links1`](../../doc/models/links-1.md) | Optional | References to resources connected with this user. | getLinks(): ?Links1 | setLinks(?Links1 links): void |
| `accountGroups` | `?(string[])` | Optional | The list of [account groups](https://docs.adyen.com/account/account-structure#account-groups) associated with this user. | getAccountGroups(): ?array | setAccountGroups(?array accountGroups): void |
| `active` | `?bool` | Optional | Indicates whether this user is active. | getActive(): ?bool | setActive(?bool active): void |
| `apps` | `?(string[])` | Optional | Set of apps available to this user | getApps(): ?array | setApps(?array apps): void |
| `email` | `string` | Required | The email address of the user. | getEmail(): string | setEmail(string email): void |
| `id` | `string` | Required | The unique identifier of the user. | getId(): string | setId(string id): void |
| `name` | [`?Name`](../../doc/models/name.md) | Optional | The user's full name. | getName(): ?Name | setName(?Name name): void |
| `roles` | `string[]` | Required | The list of [roles](https://docs.adyen.com/account/user-roles) for this user. | getRoles(): array | setRoles(array roles): void |
| `timeZoneCode` | `string` | Required | The [tz database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) of the time zone of the user. For example, **Europe/Amsterdam**. | getTimeZoneCode(): string | setTimeZoneCode(string timeZoneCode): void |
| `username` | `string` | Required | The username for this user.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getUsername(): string | setUsername(string username): void |

## Example (as JSON)

```json
{
  "_links": {
    "self": {
      "href": "href0"
    }
  },
  "accountGroups": [
    "accountGroups1",
    "accountGroups0"
  ],
  "active": false,
  "apps": [
    "apps0"
  ],
  "email": "email0",
  "id": "id6",
  "name": {
    "firstName": "firstName4",
    "lastName": "lastName4"
  },
  "roles": [
    "roles2",
    "roles1"
  ],
  "timeZoneCode": "timeZoneCode8",
  "username": "username6"
}
```

