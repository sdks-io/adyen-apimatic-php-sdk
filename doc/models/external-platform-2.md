
# External Platform 2

Third-party developed platform used to initiate payment requests. For example, Magento, Zuora, etc.

## Structure

`ExternalPlatform2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `integrator` | `?string` | Optional | External platform integrator. | getIntegrator(): ?string | setIntegrator(?string integrator): void |
| `name` | `?string` | Optional | Name of the field. For example, Name of External Platform. | getName(): ?string | setName(?string name): void |
| `version` | `?string` | Optional | Version of the field. For example, Version of External Platform. | getVersion(): ?string | setVersion(?string version): void |

## Example (as JSON)

```json
{
  "integrator": "integrator4",
  "name": "name8",
  "version": "version4"
}
```

