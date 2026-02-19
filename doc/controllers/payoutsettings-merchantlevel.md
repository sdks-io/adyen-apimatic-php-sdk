# Payoutsettings-Merchantlevel

```php
$payoutsettingsMerchantlevelApi = $client->getPayoutsettingsMerchantlevelApi();
```

## Class Name

`PayoutsettingsMerchantlevelApi`

## Methods

* [Get-Merchants-Merchant Id-Payout Settings](../../doc/controllers/payoutsettings-merchantlevel.md#get-merchants-merchant-id-payout-settings)
* [Post-Merchants-Merchant Id-Payout Settings](../../doc/controllers/payoutsettings-merchantlevel.md#post-merchants-merchant-id-payout-settings)
* [Delete-Merchants-Merchant Id-Payout Settings-Payout Settings Id](../../doc/controllers/payoutsettings-merchantlevel.md#delete-merchants-merchant-id-payout-settings-payout-settings-id)
* [Get-Merchants-Merchant Id-Payout Settings-Payout Settings Id](../../doc/controllers/payoutsettings-merchantlevel.md#get-merchants-merchant-id-payout-settings-payout-settings-id)
* [Patch-Merchants-Merchant Id-Payout Settings-Payout Settings Id](../../doc/controllers/payoutsettings-merchantlevel.md#patch-merchants-merchant-id-payout-settings-payout-settings-id)


# Get-Merchants-Merchant Id-Payout Settings

Returns the list of payout settings for the merchant account identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read

```php
function getMerchantsMerchantIdPayoutSettings(string $merchantId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PayoutSettingsResponse`](../../doc/models/payout-settings-response.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$payoutSettingsMerchantLevelApi = $client->getPayoutSettingsMerchantLevelApi();
$apiResponse = $payoutSettingsMerchantLevelApi->getMerchantsMerchantIdPayoutSettings($merchantId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PayoutSettingsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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


# Post-Merchants-Merchant Id-Payout Settings

Sends a request to add a payout setting for the merchant account specified in the path. A payout setting links the merchant account to the [transfer instrument](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/transferInstruments) that contains the details of the payout bank account. Adyen verifies the bank account before allowing and enabling the payout setting.

If you're accepting payments in multiple currencies, you may add multiple payout settings for the merchant account.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```php
function postMerchantsMerchantIdPayoutSettings(
    string $merchantId,
    ?PayoutSettingsRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`?PayoutSettingsRequest`](../../doc/models/payout-settings-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$payoutSettingsMerchantLevelApi = $client->getPayoutSettingsMerchantLevelApi();
$apiResponse = $payoutSettingsMerchantLevelApi->postMerchantsMerchantIdPayoutSettings($merchantId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PayoutSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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


# Delete-Merchants-Merchant Id-Payout Settings-Payout Settings Id

Deletes the payout setting identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```php
function deleteMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    string $merchantId,
    string $payoutSettingsId
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `payoutSettingsId` | `string` | Template, Required | The unique identifier of the payout setting. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```php
$merchantId = 'merchantId6';

$payoutSettingsId = 'payoutSettingsId6';

$payoutSettingsMerchantLevelApi = $client->getPayoutSettingsMerchantLevelApi();
$apiResponse = $payoutSettingsMerchantLevelApi->deleteMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    $merchantId,
    $payoutSettingsId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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


# Get-Merchants-Merchant Id-Payout Settings-Payout Settings Id

Returns the payout setting identified in the path.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read

```php
function getMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    string $merchantId,
    string $payoutSettingsId
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `payoutSettingsId` | `string` | Template, Required | The unique identifier of the payout setting. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$payoutSettingsId = 'payoutSettingsId6';

$payoutSettingsMerchantLevelApi = $client->getPayoutSettingsMerchantLevelApi();
$apiResponse = $payoutSettingsMerchantLevelApi->getMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    $merchantId,
    $payoutSettingsId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PayoutSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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


# Patch-Merchants-Merchant Id-Payout Settings-Payout Settings Id

Updates the payout setting identified in the path. You can enable or disable the payout setting.

Use this endpoint if your integration requires it, such as Adyen for Platforms Manage. Your Adyen contact will set up your access.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payout account settings read and write

```php
function patchMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    string $merchantId,
    string $payoutSettingsId,
    ?UpdatePayoutSettingsRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `payoutSettingsId` | `string` | Template, Required | The unique identifier of the payout setting. |
| `body` | [`?UpdatePayoutSettingsRequest`](../../doc/models/update-payout-settings-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PayoutSettings`](../../doc/models/payout-settings.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$payoutSettingsId = 'payoutSettingsId6';

$payoutSettingsMerchantLevelApi = $client->getPayoutSettingsMerchantLevelApi();
$apiResponse = $payoutSettingsMerchantLevelApi->patchMerchantsMerchantIdPayoutSettingsPayoutSettingsId(
    $merchantId,
    $payoutSettingsId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PayoutSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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

