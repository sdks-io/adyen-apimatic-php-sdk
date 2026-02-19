
# Notification 2

Configures sending event notifications by pressing a button on a terminal, for example used for pay-at-table.

## Structure

`Notification2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `category` | [`?string(Category)`](../../doc/models/category.md) | Optional | The type of event notification sent when you select the notification button. | getCategory(): ?string | setCategory(?string category): void |
| `details` | `?string` | Optional | The text shown in the prompt which opens when you select the notification button. For example, the description of the input box for pay-at-table. | getDetails(): ?string | setDetails(?string details): void |
| `enabled` | `?bool` | Optional | Enables sending event notifications either by pressing the Confirm key on terminals with a keypad or by tapping the event notification button on the terminal screen. | getEnabled(): ?bool | setEnabled(?bool enabled): void |
| `showButton` | `?bool` | Optional | Shows or hides the event notification button on the screen of terminal models that have a keypad. | getShowButton(): ?bool | setShowButton(?bool showButton): void |
| `title` | `?string` | Optional | The name of the notification button on the terminal screen. | getTitle(): ?string | setTitle(?string title): void |

## Example (as JSON)

```json
{
  "category": "SaleWakeUp",
  "details": "details8",
  "enabled": false,
  "showButton": false,
  "title": "title6"
}
```

