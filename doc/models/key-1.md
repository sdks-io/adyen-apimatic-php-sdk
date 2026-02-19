
# Key 1

The key you share with Adyen to secure local communications when using Terminal API.

## Structure

`Key1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `identifier` | `?string` | Optional | The unique identifier of the shared key. | getIdentifier(): ?string | setIdentifier(?string identifier): void |
| `passphrase` | `?string` | Optional | The secure passphrase to protect the shared key. Must consist of:<br><br>* At least 12 characters.<br><br>* At least 1 uppercase letter: `[A-Z]`.<br><br>* At least 1 lowercase letter: `[a-z]`.<br><br>* At least 1 digit: `[0-9]`.<br><br>* At least 1 special character. Limited to the following: `~`, `!`, `@`, `#`, `$`, `%`, `^`, `&`, `*`, `(`, `)`, `_`, `+`, `=`, `}`, `{`, `]`, `[`, `;`, `:`, `?`, `.`, `,`, `>`, `<`. | getPassphrase(): ?string | setPassphrase(?string passphrase): void |
| `version` | `?int` | Optional | The version number of the shared key. | getVersion(): ?int | setVersion(?int version): void |

## Example (as JSON)

```json
{
  "identifier": "identifier2",
  "passphrase": "passphrase0",
  "version": 64
}
```

