
# Update Company User Request

## Structure

`UpdateCompanyUserRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountGroups` | `?(string[])` | Optional | The list of [account groups](https://docs.adyen.com/account/account-structure#account-groups) associated with this user. | getAccountGroups(): ?array | setAccountGroups(?array accountGroups): void |
| `active` | `?bool` | Optional | Indicates whether this user is active. | getActive(): ?bool | setActive(?bool active): void |
| `associatedMerchantAccounts` | `?(string[])` | Optional | The list of [merchant accounts](https://docs.adyen.com/account/account-structure#merchant-accounts) to associate the user with. | getAssociatedMerchantAccounts(): ?array | setAssociatedMerchantAccounts(?array associatedMerchantAccounts): void |
| `email` | `?string` | Optional | The email address of the user. | getEmail(): ?string | setEmail(?string email): void |
| `loginMethod` | `?string` | Optional | The requested login method for the user. To use SSO, you must already have SSO configured with Adyen before creating the user.<br><br>Possible values: **Username & account**, **Email**, or **SSO** | getLoginMethod(): ?string | setLoginMethod(?string loginMethod): void |
| `name` | [`?Name22`](../../doc/models/name-22.md) | Optional | The user's full name. | getName(): ?Name22 | setName(?Name22 name): void |
| `roles` | `?(string[])` | Optional | The list of [roles](https://docs.adyen.com/account/user-roles) for this user. | getRoles(): ?array | setRoles(?array roles): void |
| `timeZoneCode` | `?string` | Optional | The [tz database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) of the time zone of the user. For example, **Europe/Amsterdam**. | getTimeZoneCode(): ?string | setTimeZoneCode(?string timeZoneCode): void |

## Example (as JSON)

```json
{
  "accountGroups": [
    "accountGroups3",
    "accountGroups4",
    "accountGroups5"
  ],
  "active": false,
  "associatedMerchantAccounts": [
    "associatedMerchantAccounts6"
  ],
  "email": "email0",
  "loginMethod": "loginMethod8"
}
```

