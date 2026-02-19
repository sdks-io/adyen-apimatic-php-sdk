
# We Chat Pay Mini Program

*This model accepts additional fields of type array.*

## Structure

`WeChatPayMiniProgram`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appId` | `?string` | Optional | - | getAppId(): ?string | setAppId(?string appId): void |
| `checkoutAttemptId` | `?string` | Optional | The checkout attempt identifier. | getCheckoutAttemptId(): ?string | setCheckoutAttemptId(?string checkoutAttemptId): void |
| `openid` | `?string` | Optional | - | getOpenid(): ?string | setOpenid(?string openid): void |
| `recurringDetailReference` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token. | getRecurringDetailReference(): ?string | setRecurringDetailReference(?string recurringDetailReference): void |
| `sdkData` | `?string` | Optional | Base64-encoded JSON object containing SDK related parameters required by the SDK<br><br>**Constraints**: *Maximum Length*: `50000` | getSdkData(): ?string | setSdkData(?string sdkData): void |
| `storedPaymentMethodId` | `?string` | Optional | This is the `recurringDetailReference` returned in the response when you created the token.<br><br>**Constraints**: *Maximum Length*: `64` | getStoredPaymentMethodId(): ?string | setStoredPaymentMethodId(?string storedPaymentMethodId): void |
| `type` | [`?string(Type51)`](../../doc/models/type-51.md) | Optional | **wechatpayMiniProgram**<br><br>**Default**: `Type51::WECHATPAYMINIPROGRAM` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example (as JSON)

```json
{
  "type": "wechatpayMiniProgram",
  "appId": "appId2",
  "checkoutAttemptId": "checkoutAttemptId2",
  "openid": "openid6",
  "recurringDetailReference": "recurringDetailReference6",
  "sdkData": "sdkData6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

