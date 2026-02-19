
# Url

## Structure

`Url`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `encrypted` | `?bool` | Optional | Indicates if the message sent to this URL should be encrypted. | getEncrypted(): ?bool | setEncrypted(?bool encrypted): void |
| `password` | `?string` | Optional | The password for authentication of the notifications. | getPassword(): ?string | setPassword(?string password): void |
| `url` | `?string` | Optional | The URL in the format: http(s)://domain.com. | getUrl(): ?string | setUrl(?string url): void |
| `username` | `?string` | Optional | The username for authentication of the notifications. | getUsername(): ?string | setUsername(?string username): void |

## Example (as JSON)

```json
{
  "encrypted": false,
  "password": "password6",
  "url": "url6",
  "username": "username2"
}
```

