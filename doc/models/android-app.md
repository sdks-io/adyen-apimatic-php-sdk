
# Android App

## Structure

`AndroidApp`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | The description that was provided when uploading the app. The description is not shown on the terminal. | getDescription(): ?string | setDescription(?string description): void |
| `errorCode` | `?string` | Optional | The error code of the Android app with the `status` of either **error** or **invalid**. | getErrorCode(): ?string | setErrorCode(?string errorCode): void |
| `errors` | [`?(AndroidAppError[])`](../../doc/models/android-app-error.md) | Optional | The list of errors of the Android app. | getErrors(): ?array | setErrors(?array errors): void |
| `id` | `string` | Required | The unique identifier of the app. | getId(): string | setId(string id): void |
| `label` | `?string` | Optional | The app name that is shown on the terminal. | getLabel(): ?string | setLabel(?string label): void |
| `packageName` | `?string` | Optional | The package name that uniquely identifies the Android app. | getPackageName(): ?string | setPackageName(?string packageName): void |
| `status` | [`string(Status5)`](../../doc/models/status-5.md) | Required | The status of the app. Possible values:<br><br>* `processing`: the app is being signed and converted to a format that the terminal can handle.<br>* `error`: something went wrong. Check that the app matches the [requirements](https://docs.adyen.com/point-of-sale/android-terminals/app-requirements).<br>* `invalid`: there is something wrong with the APK file of the app.<br>* `ready`: the app has been signed and converted.<br>* `archived`: the app is no longer available. | getStatus(): string | setStatus(string status): void |
| `versionCode` | `?int` | Optional | The version number of the app. | getVersionCode(): ?int | setVersionCode(?int versionCode): void |
| `versionName` | `?string` | Optional | The app version number that is shown on the terminal. | getVersionName(): ?string | setVersionName(?string versionName): void |

## Example (as JSON)

```json
{
  "description": "description0",
  "errorCode": "errorCode6",
  "errors": [
    {
      "errorCode": "errorCode6",
      "terminalModels": [
        "terminalModels3",
        "terminalModels4"
      ]
    },
    {
      "errorCode": "errorCode6",
      "terminalModels": [
        "terminalModels3",
        "terminalModels4"
      ]
    }
  ],
  "id": "id0",
  "label": "label0",
  "packageName": "packageName6",
  "status": "invalid"
}
```

