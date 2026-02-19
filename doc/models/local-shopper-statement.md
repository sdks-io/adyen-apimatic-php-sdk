
# Local Shopper Statement

## Structure

`LocalShopperStatement`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `script` | `string` | Required | The character set of the local shopper statement.<br><br>Possible values: **ja-Hani**, **ja-Kana**. | getScript(): string | setScript(string script): void |
| `value` | `string` | Required | The text of the local shopper statement in the specified character set. | getValue(): string | setValue(string value): void |

## Example (as JSON)

```json
{
  "script": "script0",
  "value": "value2"
}
```

