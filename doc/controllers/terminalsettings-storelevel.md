# Terminalsettings-Storelevel

```php
$terminalsettingsStorelevelApi = $client->getTerminalsettingsStorelevelApi();
```

## Class Name

`TerminalsettingsStorelevelApi`

## Methods

* [Get Merchant Store Terminal Logo by Reference](../../doc/controllers/terminalsettings-storelevel.md#get-merchant-store-terminal-logo-by-reference)
* [Update Merchant Store Terminal Logo by Reference](../../doc/controllers/terminalsettings-storelevel.md#update-merchant-store-terminal-logo-by-reference)
* [Get Merchant Store Terminal Settings by Reference](../../doc/controllers/terminalsettings-storelevel.md#get-merchant-store-terminal-settings-by-reference)
* [Update Merchant Store Terminal Settings by Reference](../../doc/controllers/terminalsettings-storelevel.md#update-merchant-store-terminal-settings-by-reference)
* [Get Store Terminal Logo](../../doc/controllers/terminalsettings-storelevel.md#get-store-terminal-logo)
* [Update Store Terminal Logo](../../doc/controllers/terminalsettings-storelevel.md#update-store-terminal-logo)
* [Get Store Terminal Settings](../../doc/controllers/terminalsettings-storelevel.md#get-store-terminal-settings)
* [Update Store Terminal Settings](../../doc/controllers/terminalsettings-storelevel.md#update-store-terminal-settings)


# Get Merchant Store Terminal Logo by Reference

Returns the logo that is configured for a specific payment terminal model at the store identified in the path.
The logo is returned as a Base64-encoded string. You need to Base64-decode the string to get the actual image file.
This logo applies to all terminals of the specified model under the store, unless a different logo is configured for an individual terminal.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read
* Management API—Terminal settings read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getMerchantStoreTerminalLogoByReference(
    string $merchantId,
    string $reference,
    string $model
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `reference` | `string` | Template, Required | The reference that identifies the store. |
| `model` | `string` | Query, Required | The terminal model. Possible values: E355, VX675WIFIBT, VX680, VX690, VX700, VX820, M400, MX925, P400Plus, UX300, UX410, V200cPlus, V240mPlus, V400cPlus, V400m, e280, e285, e285p, S1E, S1EL, S1F2, S1L, S1U, S7T. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Logo`](../../doc/models/logo.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$reference = 'reference4';

$model = 'model2';

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->getMerchantStoreTerminalLogoByReference(
    $merchantId,
    $reference,
    $model
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Logo:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": "BASE-64_ENCODED_STRING"
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


# Update Merchant Store Terminal Logo by Reference

Updates the logo that is configured for a specific payment terminal model at the store identified in the path. You can update the logo for only one terminal model at a time.
This logo applies to all terminals of the specified model under the store, unless a different logo is configured for an individual terminal.

* To change the logo, specify the image file as a Base64-encoded string.
* To restore the logo inherited from a higher level (merchant or company account), specify an empty logo value.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function updateMerchantStoreTerminalLogoByReference(
    string $merchantId,
    string $reference,
    string $model,
    ?Logo $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `reference` | `string` | Template, Required | The reference that identifies the store. |
| `model` | `string` | Query, Required | The terminal model. Possible values: E355, VX675WIFIBT, VX680, VX690, VX700, VX820, M400, MX925, P400Plus, UX300, UX410, V200cPlus, V240mPlus, V400cPlus, V400m, e280, e285, e285p, S1E, S1EL, S1F2, S1L, S1U, S7T |
| `body` | [`?Logo`](../../doc/models/logo.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Logo`](../../doc/models/logo.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$reference = 'reference4';

$model = 'model2';

$body = LogoBuilder::init()
    ->data('')
    ->build();

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->updateMerchantStoreTerminalLogoByReference(
    $merchantId,
    $reference,
    $model,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Logo:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": "LOGO_INHERITED_FROM_HIGHER_LEVEL_BASE-64_ENCODED_STRING"
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


# Get Merchant Store Terminal Settings by Reference

Returns the payment terminal settings that are configured for the store identified in the path. These settings apply to all terminals under the store unless different values are configured for an individual terminal.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read
* Management API—Terminal settings read and write

For [sensitive terminal settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings), your API credential must have the following role:

* Management API—Terminal settings Advanced read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getMerchantStoreTerminalSettingsByReference(string $merchantId, string $reference): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `reference` | `string` | Template, Required | The reference that identifies the store. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`TerminalSettings`](../../doc/models/terminal-settings.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$reference = 'reference4';

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->getMerchantStoreTerminalSettingsByReference(
    $merchantId,
    $reference
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'TerminalSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "cardholderReceipt": {
    "headerForAuthorizedReceipt": "header1,header2,filler"
  },
  "gratuities": [
    {
      "currency": "EUR",
      "usePredefinedTipEntries": true,
      "predefinedTipEntries": [
        "100",
        "1%",
        "5%"
      ],
      "allowCustomAmount": true
    }
  ],
  "nexo": {
    "nexoEventUrls": [
      "https://your-event-notifications-endpoint.com"
    ]
  },
  "opi": {
    "enablePayAtTable": true,
    "payAtTableStoreNumber": "1",
    "payAtTableURL": "https:/your-pay-at-table-endpoint.com"
  },
  "receiptOptions": {},
  "receiptPrinting": {
    "shopperApproved": true,
    "shopperRefused": true,
    "shopperCancelled": true,
    "shopperRefundApproved": true,
    "shopperRefundRefused": true,
    "shopperVoid": true
  },
  "signature": {
    "askSignatureOnScreen": true,
    "skipSignature": false,
    "deviceName": "Amsterdam-236203386"
  },
  "wifiProfiles": {
    "profiles": [
      {
        "authType": "wpa-psk",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": true,
        "name": "Guest Wi-Fi",
        "psk": "4R8R2R3V456X",
        "ssid": "G470P37660D4G",
        "wsec": "ccmp"
      }
    ],
    "settings": {
      "band": "All",
      "roaming": true
    }
  },
  "timeouts": {
    "fromActiveToSleep": 30
  },
  "hardware": {
    "displayMaximumBackLight": 75
  },
  "passcodes": {
    "adminMenuPin": "1234",
    "txMenuPin": "1234",
    "screenLockPin": "1234"
  },
  "storeAndForward": {
    "maxAmount": [
      {
        "amount": 10000,
        "currencyCode": "EUR"
      }
    ],
    "maxPayments": 10,
    "supportedCardTypes": {
      "credit": true,
      "debit": true,
      "deferredDebit": true,
      "prepaid": true,
      "unknown": false
    }
  },
  "terminalInstructions": {
    "adyenAppRestart": true
  }
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


# Update Merchant Store Terminal Settings by Reference

Updates payment terminal settings for the store identified in the path. These settings apply to all terminals under the store, unless different values are configured for an individual terminal.

* To change a parameter value, include the full object that contains the parameter, even if you don't want to change all parameters in the object.
* To restore a parameter value inherited from a higher level, include the full object that contains the parameter, and specify an empty value for the parameter or omit the parameter.
* Objects that are not included in the request are not updated.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read and write

For [sensitive terminal settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings), your API credential must have the following role:

* Management API—Terminal settings Advanced read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function updateMerchantStoreTerminalSettingsByReference(
    string $merchantId,
    string $reference,
    ?TerminalSettings $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `reference` | `string` | Template, Required | The reference that identifies the store. |
| `body` | [`?TerminalSettings`](../../doc/models/terminal-settings.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`TerminalSettings`](../../doc/models/terminal-settings.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$reference = 'reference4';

$body = TerminalSettingsBuilder::init()
    ->wifiProfiles(
        WifiProfiles2Builder::init()
            ->profiles(
                [
                    ProfileBuilder::init(
                        'wpa-eap',
                        'infra',
                        'your-network',
                        'ccmp'
                    )
                        ->autoWifi(false)
                        ->channel(0)
                        ->defaultProfile(true)
                        ->eap('peap')
                        ->eapCaCert(
                            File1Builder::init(
                                'MD1rKS05M2JqRVFNQ...RTtLH1tLWo=',
                                'eap-peap-ca.pem'
                            )->build()
                        )
                        ->eapIdentity('admin')
                        ->eapIntermediateCert(
                            File4Builder::init(
                                'PD3tUS1CRDdJTiGDR...EFoLS0tLQg=',
                                'eap-peap-client.pem'
                            )->build()
                        )
                        ->eapPwd('EAP_PEAP_PASSWORD')
                        ->name('Profile-eap-peap-1')
                        ->build(),
                    ProfileBuilder::init(
                        'wpa-psk',
                        'infra',
                        'your-network',
                        'ccmp'
                    )
                        ->autoWifi(false)
                        ->channel(0)
                        ->defaultProfile(false)
                        ->name('Profile-guest-wifi')
                        ->psk('WIFI_PASSWORD')
                        ->build()
                ]
            )
            ->settings(
                Settings1Builder::init()
                    ->band('2.4GHz')
                    ->roaming(true)
                    ->timeout(5)
                    ->build()
            )
            ->build()
    )
    ->build();

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->updateMerchantStoreTerminalSettingsByReference(
    $merchantId,
    $reference,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'TerminalSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "cardholderReceipt": {
    "headerForAuthorizedReceipt": "header1,header2,filler"
  },
  "gratuities": [
    {
      "currency": "EUR",
      "usePredefinedTipEntries": true,
      "predefinedTipEntries": [
        "100",
        "1%",
        "5%"
      ],
      "allowCustomAmount": true
    }
  ],
  "nexo": {
    "displayUrls": {
      "localUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-display-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    },
    "encryptionKey": {
      "identifier": "KEY_IDENTIFIER",
      "passphrase": "KEY_PASSPHRASE",
      "version": 1
    },
    "eventUrls": {
      "eventPublicUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-event-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    }
  },
  "opi": {
    "enablePayAtTable": true,
    "payAtTableStoreNumber": "1",
    "payAtTableURL": "https:/your-pay-at-table-endpoint.com"
  },
  "offlineProcessing": {
    "chipFloorLimit": 0
  },
  "receiptOptions": {
    "qrCodeData": "http://www.example.com/order/${pspreference}/${merchantreference}"
  },
  "receiptPrinting": {
    "shopperApproved": true,
    "shopperRefused": true,
    "shopperCancelled": true,
    "shopperRefundApproved": true,
    "shopperRefundRefused": true,
    "shopperVoid": true
  },
  "signature": {
    "askSignatureOnScreen": true,
    "skipSignature": false,
    "deviceName": "Amsterdam-236203386"
  },
  "wifiProfiles": {
    "profiles": [
      {
        "authType": "wpa-eap",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": true,
        "eap": "peap",
        "eapCaCert": {
          "data": "MD1rKS05M2JqRVFNQ...RTtLH1tLWo=",
          "name": "eap-peap-ca.pem"
        },
        "eapIdentity": "admin",
        "eapIntermediateCert": {
          "data": "PD3tUS1CRDdJTiGDR...EFoLS0tLQg=",
          "name": "eap-peap-client.pem"
        },
        "eapPwd": "EAP_PEAP_PASSWORD",
        "name": "Profile-eap-peap-1",
        "ssid": "your-network",
        "wsec": "ccmp"
      },
      {
        "authType": "wpa-psk",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": false,
        "name": "Profile-guest-wifi",
        "psk": "WIFI_PASSWORD",
        "ssid": "your-network",
        "wsec": "ccmp"
      }
    ],
    "settings": {
      "band": "2.4GHz",
      "roaming": true,
      "timeout": 5
    }
  },
  "timeouts": {
    "fromActiveToSleep": 30
  },
  "hardware": {
    "displayMaximumBackLight": 75
  }
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


# Get Store Terminal Logo

Returns the logo that is configured for a specific payment terminal model at the store identified in the path.
The logo is returned as a Base64-encoded string. You need to Base64-decode the string to get the actual image file.
This logo applies to all terminals of that model under the store unless a different logo is configured for an individual terminal.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read
* Management API—Terminal settings read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getStoreTerminalLogo(string $storeId, string $model): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |
| `model` | `string` | Query, Required | The terminal model. Possible values: E355, VX675WIFIBT, VX680, VX690, VX700, VX820, M400, MX925, P400Plus, UX300, UX410, V200cPlus, V240mPlus, V400cPlus, V400m, e280, e285, e285p, S1E, S1EL, S1F2, S1L, S1U, S7T. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Logo`](../../doc/models/logo.md).

## Example Usage

```php
$storeId = 'storeId6';

$model = 'model2';

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->getStoreTerminalLogo(
    $storeId,
    $model
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Logo:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": "BASE-64_ENCODED_STRING"
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


# Update Store Terminal Logo

Updates the logo that is configured for a specific payment terminal model at the store identified in the path. You can update the logo for only one terminal model at a time.
This logo applies to all terminals of the specified model under the store, unless a different logo is configured for an individual terminal.

* To change the logo, specify the image file as a Base64-encoded string.
* To restore the logo inherited from a higher level (merchant or company account), specify an empty logo value.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function updateStoreTerminalLogo(string $storeId, string $model, ?Logo $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |
| `model` | `string` | Query, Required | The terminal model. Possible values: E355, VX675WIFIBT, VX680, VX690, VX700, VX820, M400, MX925, P400Plus, UX300, UX410, V200cPlus, V240mPlus, V400cPlus, V400m, e280, e285, e285p, S1E, S1EL, S1F2, S1L, S1U, S7T. |
| `body` | [`?Logo`](../../doc/models/logo.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Logo`](../../doc/models/logo.md).

## Example Usage

```php
$storeId = 'storeId6';

$model = 'model2';

$body = LogoBuilder::init()
    ->data('')
    ->build();

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->updateStoreTerminalLogo(
    $storeId,
    $model,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Logo:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": "LOGO_INHERITED_FROM_HIGHER_LEVEL_BASE-64_ENCODED_STRING"
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


# Get Store Terminal Settings

Returns the payment terminal settings that are configured for the store identified in the path. These settings apply to all terminals under the store unless different values are configured for an individual terminal.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read
* Management API—Terminal settings read and write

For [sensitive terminal settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings), your API credential must have the following role:

* Management API—Terminal settings Advanced read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getStoreTerminalSettings(string $storeId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`TerminalSettings`](../../doc/models/terminal-settings.md).

## Example Usage

```php
$storeId = 'storeId6';

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->getStoreTerminalSettings($storeId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'TerminalSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "cardholderReceipt": {
    "headerForAuthorizedReceipt": "header1,header2,filler"
  },
  "gratuities": [
    {
      "currency": "EUR",
      "usePredefinedTipEntries": true,
      "predefinedTipEntries": [
        "100",
        "1%",
        "5%"
      ],
      "allowCustomAmount": true
    }
  ],
  "nexo": {
    "displayUrls": {
      "localUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-display-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    },
    "encryptionKey": {
      "identifier": "KEY_IDENTIFIER",
      "passphrase": "KEY_PASSPHRASE",
      "version": 1
    },
    "eventUrls": {
      "eventPublicUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-event-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    }
  },
  "opi": {
    "enablePayAtTable": true,
    "payAtTableStoreNumber": "1",
    "payAtTableURL": "https:/your-pay-at-table-endpoint.com"
  },
  "offlineProcessing": {
    "chipFloorLimit": 0
  },
  "receiptOptions": {
    "qrCodeData": "http://www.example.com/order/${pspreference}/${merchantreference}"
  },
  "receiptPrinting": {
    "shopperApproved": true,
    "shopperRefused": true,
    "shopperCancelled": true,
    "shopperRefundApproved": true,
    "shopperRefundRefused": true,
    "shopperVoid": true
  },
  "signature": {
    "askSignatureOnScreen": true,
    "skipSignature": false,
    "deviceName": "Amsterdam-236203386"
  },
  "wifiProfiles": {
    "profiles": [
      {
        "authType": "wpa-psk",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": true,
        "hiddenSsid": false,
        "name": "Guest Wi-Fi",
        "psk": "4R8R2R3V456X",
        "ssid": "G470P37660D4G",
        "wsec": "ccmp"
      }
    ],
    "settings": {
      "band": "All",
      "roaming": true
    }
  },
  "timeouts": {
    "fromActiveToSleep": 30
  },
  "hardware": {
    "displayMaximumBackLight": 75
  },
  "passcodes": {
    "adminMenuPin": "1234",
    "txMenuPin": "1234",
    "screenLockPin": "1234"
  },
  "storeAndForward": {
    "maxAmount": [
      {
        "amount": 10000,
        "currencyCode": "EUR"
      }
    ],
    "maxPayments": 10,
    "supportedCardTypes": {
      "credit": true,
      "debit": true,
      "deferredDebit": true,
      "prepaid": true,
      "unknown": false
    }
  },
  "terminalInstructions": {
    "adyenAppRestart": true
  }
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


# Update Store Terminal Settings

Updates payment terminal settings for the store identified in the path. These settings apply to all terminals under the store, unless different values are configured for an individual terminal.

* To change a parameter value, include the full object that contains the parameter, even if you don't want to change all parameters in the object.
* To restore a parameter value inherited from a higher level, include the full object that contains the parameter, and specify an empty value for the parameter or omit the parameter.
* Objects that are not included in the request are not updated.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Terminal settings read and write

For [sensitive terminal settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings), your API credential must have the following role:

* Management API—Terminal settings Advanced read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function updateStoreTerminalSettings(string $storeId, ?TerminalSettings $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |
| `body` | [`?TerminalSettings`](../../doc/models/terminal-settings.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`TerminalSettings`](../../doc/models/terminal-settings.md).

## Example Usage

```php
$storeId = 'storeId6';

$body = TerminalSettingsBuilder::init()
    ->wifiProfiles(
        WifiProfiles2Builder::init()
            ->profiles(
                [
                    ProfileBuilder::init(
                        'wpa-eap',
                        'infra',
                        'your-network',
                        'ccmp'
                    )
                        ->autoWifi(false)
                        ->channel(0)
                        ->defaultProfile(true)
                        ->eap('peap')
                        ->eapCaCert(
                            File1Builder::init(
                                'MD1rKS05M2JqRVFNQ...RTtLH1tLWo=',
                                'eap-peap-ca.pem'
                            )->build()
                        )
                        ->eapIdentity('admin')
                        ->eapIntermediateCert(
                            File4Builder::init(
                                'PD3tUS1CRDdJTiGDR...EFoLS0tLQg=',
                                'eap-peap-client.pem'
                            )->build()
                        )
                        ->eapPwd('EAP_PEAP_PASSWORD')
                        ->hiddenSsid(false)
                        ->name('Profile-eap-peap-1')
                        ->build(),
                    ProfileBuilder::init(
                        'wpa-psk',
                        'infra',
                        'your-network',
                        'ccmp'
                    )
                        ->autoWifi(false)
                        ->channel(0)
                        ->defaultProfile(false)
                        ->hiddenSsid(false)
                        ->name('Profile-guest-wifi')
                        ->psk('WIFI_PASSWORD')
                        ->build()
                ]
            )
            ->settings(
                Settings1Builder::init()
                    ->band('2.4GHz')
                    ->roaming(true)
                    ->timeout(5)
                    ->build()
            )
            ->build()
    )
    ->build();

$terminalSettingsStoreLevelApi = $client->getTerminalSettingsStoreLevelApi();
$apiResponse = $terminalSettingsStoreLevelApi->updateStoreTerminalSettings(
    $storeId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'TerminalSettings:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "cardholderReceipt": {
    "headerForAuthorizedReceipt": "header1,header2,filler"
  },
  "gratuities": [
    {
      "currency": "EUR",
      "usePredefinedTipEntries": true,
      "predefinedTipEntries": [
        "100",
        "1%",
        "5%"
      ],
      "allowCustomAmount": true
    }
  ],
  "nexo": {
    "displayUrls": {
      "localUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-display-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    },
    "encryptionKey": {
      "identifier": "KEY_IDENTIFIER",
      "passphrase": "KEY_PASSPHRASE",
      "version": 1
    },
    "eventUrls": {
      "eventPublicUrls": [
        {
          "password": "BASIC_AUTH_PASSWORD",
          "url": "https://your-event-notifications-endpoint.com",
          "username": "BASIC_AUTH_USERNAME"
        }
      ]
    }
  },
  "opi": {
    "enablePayAtTable": true,
    "payAtTableStoreNumber": "1",
    "payAtTableURL": "https:/your-pay-at-table-endpoint.com"
  },
  "offlineProcessing": {
    "chipFloorLimit": 0
  },
  "receiptOptions": {
    "qrCodeData": "http://www.example.com/order/${pspreference}/${merchantreference}"
  },
  "receiptPrinting": {
    "shopperApproved": true,
    "shopperRefused": true,
    "shopperCancelled": true,
    "shopperRefundApproved": true,
    "shopperRefundRefused": true,
    "shopperVoid": true
  },
  "signature": {
    "askSignatureOnScreen": true,
    "skipSignature": false,
    "deviceName": "Amsterdam-236203386"
  },
  "wifiProfiles": {
    "profiles": [
      {
        "authType": "wpa-eap",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": true,
        "eap": "peap",
        "eapCaCert": {
          "data": "MD1rKS05M2JqRVFNQ...RTtLH1tLWo=",
          "name": "eap-peap-ca.pem"
        },
        "eapIdentity": "admin",
        "eapIntermediateCert": {
          "data": "PD3tUS1CRDdJTiGDR...EFoLS0tLQg=",
          "name": "eap-peap-client.pem"
        },
        "eapPwd": "EAP_PEAP_PASSWORD",
        "hiddenSsid": false,
        "name": "Profile-eap-peap-1",
        "ssid": "your-network",
        "wsec": "ccmp"
      },
      {
        "authType": "wpa-psk",
        "autoWifi": false,
        "bssType": "infra",
        "channel": 0,
        "defaultProfile": false,
        "hiddenSsid": false,
        "name": "Profile-guest-wifi",
        "psk": "WIFI_PASSWORD",
        "ssid": "your-network",
        "wsec": "ccmp"
      }
    ],
    "settings": {
      "band": "2.4GHz",
      "roaming": true,
      "timeout": 5
    }
  },
  "timeouts": {
    "fromActiveToSleep": 30
  },
  "hardware": {
    "displayMaximumBackLight": 75
  }
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

