
# Sdk Ephem Pub Key 3

The `sdkEphemPubKey` value as received from the 3D Secure 2 SDK.
Required for `deviceChannel` set to **app**.

## Structure

`SdkEphemPubKey3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `crv` | `?string` | Optional | The `crv` value as received from the 3D Secure 2 SDK. | getCrv(): ?string | setCrv(?string crv): void |
| `kty` | `?string` | Optional | The `kty` value as received from the 3D Secure 2 SDK. | getKty(): ?string | setKty(?string kty): void |
| `x` | `?string` | Optional | The `x` value as received from the 3D Secure 2 SDK. | getX(): ?string | setX(?string x): void |
| `y` | `?string` | Optional | The `y` value as received from the 3D Secure 2 SDK. | getY(): ?string | setY(?string y): void |

## Example (as JSON)

```json
{
  "crv": "crv2",
  "kty": "kty2",
  "x": "x0",
  "y": "y8"
}
```

