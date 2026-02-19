
# Opi

## Structure

`Opi`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enablePayAtTable` | `?bool` | Optional | Indicates if Pay at table is enabled. | getEnablePayAtTable(): ?bool | setEnablePayAtTable(?bool enablePayAtTable): void |
| `payAtTableStoreNumber` | `?string` | Optional | The store number to use for Pay at Table. | getPayAtTableStoreNumber(): ?string | setPayAtTableStoreNumber(?string payAtTableStoreNumber): void |
| `payAtTableUrl` | `?string` | Optional | The URL and port number used for Pay at Table communication. | getPayAtTableUrl(): ?string | setPayAtTableUrl(?string payAtTableUrl): void |

## Example (as JSON)

```json
{
  "enablePayAtTable": false,
  "payAtTableStoreNumber": "payAtTableStoreNumber2",
  "payAtTableURL": "payAtTableURL0"
}
```

