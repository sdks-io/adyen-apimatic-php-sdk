
# Browser Info 2

The shopper's browser information.

> For 3D Secure, the full object is required for web integrations. For mobile app integrations, include the `userAgent` and `acceptHeader` fields to indicate  that your integration can support a redirect in case a payment is routed to 3D Secure 2 redirect.

## Structure

`BrowserInfo2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `acceptHeader` | `string` | Required | The accept header value of the shopper's browser. | getAcceptHeader(): string | setAcceptHeader(string acceptHeader): void |
| `colorDepth` | `int` | Required | The color depth of the shopper's browser in bits per pixel. This should be obtained by using the browser's `screen.colorDepth` property. Accepted values: 1, 4, 8, 15, 16, 24, 30, 32 or 48 bit color depth. | getColorDepth(): int | setColorDepth(int colorDepth): void |
| `javaEnabled` | `bool` | Required | Boolean value indicating if the shopper's browser is able to execute Java. | getJavaEnabled(): bool | setJavaEnabled(bool javaEnabled): void |
| `javaScriptEnabled` | `?bool` | Optional | Boolean value indicating if the shopper's browser is able to execute JavaScript. A default 'true' value is assumed if the field is not present.<br><br>**Default**: `true` | getJavaScriptEnabled(): ?bool | setJavaScriptEnabled(?bool javaScriptEnabled): void |
| `language` | `string` | Required | The `navigator.language` value of the shopper's browser (as defined in IETF BCP 47). | getLanguage(): string | setLanguage(string language): void |
| `screenHeight` | `int` | Required | The total height of the shopper's device screen in pixels. | getScreenHeight(): int | setScreenHeight(int screenHeight): void |
| `screenWidth` | `int` | Required | The total width of the shopper's device screen in pixels. | getScreenWidth(): int | setScreenWidth(int screenWidth): void |
| `timeZoneOffset` | `int` | Required | Time difference between UTC time and the shopper's browser local time, in minutes. | getTimeZoneOffset(): int | setTimeZoneOffset(int timeZoneOffset): void |
| `userAgent` | `string` | Required | The user agent value of the shopper's browser. | getUserAgent(): string | setUserAgent(string userAgent): void |

## Example (as JSON)

```json
{
  "acceptHeader": "acceptHeader8",
  "colorDepth": 12,
  "javaEnabled": false,
  "javaScriptEnabled": true,
  "language": "language2",
  "screenHeight": 38,
  "screenWidth": 18,
  "timeZoneOffset": 70,
  "userAgent": "userAgent6"
}
```

