# Terminalactions-Companylevel

```php
$terminalactionsCompanylevelApi = $client->getTerminalactionsCompanylevelApi();
```

## Class Name

`TerminalactionsCompanylevelApi`

## Methods

* [List Company Terminal Actions](../../doc/controllers/terminalactions-companylevel.md#list-company-terminal-actions)
* [Get Company Terminal Action](../../doc/controllers/terminalactions-companylevel.md#get-company-terminal-action)


# List Company Terminal Actions

Returns the [terminal actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api) that have been scheduled for the company identified in the path.The response doesn't include actions that are scheduled by Adyen.
To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal actions read
* Management API—Terminal actions read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function listCompanyTerminalActions(
    string $companyId,
    ?int $pageNumber = null,
    ?int $pageSize = null,
    ?string $status = null,
    ?string $type = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 20 items on a page. |
| `status` | `?string` | Query, Optional | Returns terminal actions with the specified status.<br>Allowed values: **pending**, **successful**, **failed**, **cancelled**, **tryLater**. |
| `type` | `?string` | Query, Optional | Returns terminal actions of the specified type.<br>Allowed values: **InstallAndroidApp**, **UninstallAndroidApp**, **InstallAndroidCertificate**, **UninstallAndroidCertificate**. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListExternalTerminalActionsResponse`](../../doc/models/list-external-terminal-actions-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$terminalActionsCompanyLevelApi = $client->getTerminalActionsCompanyLevelApi();
$apiResponse = $terminalActionsCompanyLevelApi->listCompanyTerminalActions($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListExternalTerminalActionsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": [
    {
      "actionType": "InstallAndroidApp",
      "config": "{\"apps\":\"com.adyen.android.calculator:103\"}",
      "confirmedAt": "2021-11-10T00:00:00+01:00",
      "id": "TRAC422T2223223K5GFMQHM6WQ4KB6",
      "result": "Cancelled manually by user USER@Psp.AdyenPspService",
      "scheduledAt": "2021-11-10T14:53:05+01:00",
      "status": "cancelled",
      "terminalId": "S1E-000150183300032"
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get Company Terminal Action

Returns the details of the [terminal action](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api) identified in the path.
To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal actions read
* Management API—Terminal actions read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getCompanyTerminalAction(string $companyId, string $actionId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `actionId` | `string` | Template, Required | The unique identifier of the terminal action. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ExternalTerminalAction`](../../doc/models/external-terminal-action.md).

## Example Usage

```php
$companyId = 'companyId0';

$actionId = 'actionId0';

$terminalActionsCompanyLevelApi = $client->getTerminalActionsCompanyLevelApi();
$apiResponse = $terminalActionsCompanyLevelApi->getCompanyTerminalAction(
    $companyId,
    $actionId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ExternalTerminalAction:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "actionType": "InstallAndroidCertificate",
  "config": "{\"certificates\":\"5dff6b...\"}",
  "confirmedAt": "2022-06-27T17:44:54+02:00",
  "id": "TRAC4224Z223223K5GD89RLBWQ6CWT",
  "result": "Ok",
  "scheduledAt": "2022-06-27T15:44:07+02:00",
  "status": "successful",
  "terminalId": "S1F2-000150183300034"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |

