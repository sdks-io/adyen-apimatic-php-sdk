
# Authentication Data 3

Data for 3DS authentication.

## Structure

`AuthenticationData3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attemptAuthentication` | [`?string(AttemptAuthentication)`](../../doc/models/attempt-authentication.md) | Optional | Indicates when 3D Secure authentication should be attempted. This overrides all other rules, including [Dynamic 3D Secure settings](https://docs.adyen.com/risk-management/dynamic-3d-secure).<br><br>Possible values:<br><br>* **always**: Perform 3D Secure authentication.<br>* **never**: Don't perform 3D Secure authentication. If PSD2 SCA or other national regulations require authentication, the transaction gets declined. | getAttemptAuthentication(): ?string | setAttemptAuthentication(?string attemptAuthentication): void |
| `authenticationOnly` | `?bool` | Optional | Required to trigger the [authentication-only flow](https://docs.adyen.com/online-payments/3d-secure/authentication-only/). If set to **true**, you will only perform the 3D Secure 2 authentication, and will not proceed to the payment authorization.<br>Default: **false**.<br><br>**Default**: `false` | getAuthenticationOnly(): ?bool | setAuthenticationOnly(?bool authenticationOnly): void |
| `threeDsRequestData` | [`?ThreeDsRequestData2`](../../doc/models/three-ds-request-data-2.md) | Optional | Object with additional parameters for the 3D Secure authentication flow. | getThreeDsRequestData(): ?ThreeDsRequestData2 | setThreeDsRequestData(?ThreeDsRequestData2 threeDsRequestData): void |

## Example (as JSON)

```json
{
  "authenticationOnly": false,
  "attemptAuthentication": "always",
  "threeDSRequestData": {
    "challengeWindowSize": "03",
    "dataOnly": "false",
    "nativeThreeDS": "preferred",
    "threeDSVersion": "2.1.0"
  }
}
```

