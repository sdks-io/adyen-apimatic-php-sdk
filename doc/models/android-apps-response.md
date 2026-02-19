
# Android Apps Response

## Structure

`AndroidAppsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(AndroidApp[])`](../../doc/models/android-app.md) | Optional | Apps uploaded for Android payment terminals. | getData(): ?array | setData(?array data): void |

## Example (as JSON)

```json
{
  "data": [
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
        }
      ],
      "id": "id0",
      "label": "label0",
      "packageName": "packageName6",
      "status": "invalid"
    }
  ]
}
```

