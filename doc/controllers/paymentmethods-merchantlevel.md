# Paymentmethods-Merchantlevel

```php
$paymentmethodsMerchantlevelApi = $client->getPaymentmethodsMerchantlevelApi();
```

## Class Name

`PaymentmethodsMerchantlevelApi`

## Methods

* [Get-Merchants-Merchant Id-Payment Method Settings](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings)
* [Post-Merchants-Merchant Id-Payment Method Settings](../../doc/controllers/paymentmethods-merchantlevel.md#post-merchants-merchant-id-payment-method-settings)
* [Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings-payment-method-id)
* [Patch-Merchants-Merchant Id-Payment Method Settings-Payment Method Id](../../doc/controllers/paymentmethods-merchantlevel.md#patch-merchants-merchant-id-payment-method-settings-payment-method-id)
* [Post-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Add Apple Pay Domains](../../doc/controllers/paymentmethods-merchantlevel.md#post-merchants-merchant-id-payment-method-settings-payment-method-id-add-apple-pay-domains)
* [Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Get Apple Pay Domains](../../doc/controllers/paymentmethods-merchantlevel.md#get-merchants-merchant-id-payment-method-settings-payment-method-id-get-apple-pay-domains)


# Get-Merchants-Merchant Id-Payment Method Settings

Returns details for all payment methods of the merchant account identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```php
function getMerchantsMerchantIdPaymentMethodSettings(
    string $merchantId,
    ?string $storeId = null,
    ?string $businessLineId = null,
    ?int $pageSize = null,
    ?int $pageNumber = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `storeId` | `?string` | Query, Optional | The unique identifier of the store for which to return the payment methods. |
| `businessLineId` | `?string` | Query, Optional | The unique identifier of the Business Line for which to return the payment methods. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PaymentMethodResponse`](../../doc/models/payment-method-response.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->getMerchantsMerchantIdPaymentMethodSettings($merchantId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PaymentMethodResponse:';
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Post-Merchants-Merchant Id-Payment Method Settings

Sends a request to add a new payment method to the merchant account identified in the path.
Depending the payment method [`type`](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings#request-type), you may need to send an additional object required for the payment method.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```php
function postMerchantsMerchantIdPaymentMethodSettings(
    string $merchantId,
    ?PaymentMethodSetupInfo $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`?PaymentMethodSetupInfo`](../../doc/models/payment-method-setup-info.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$body = PaymentMethodSetupInfoBuilder::init(
    Type410::VISA
)
    ->countries(
        [
            'US'
        ]
    )
    ->currencies(
        [
            'USD'
        ]
    )
    ->build();

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->postMerchantsMerchantIdPaymentMethodSettings(
    $merchantId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PaymentMethod1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "PM3227C223224K5FH84M8CBNH",
  "type": "visa",
  "countries": [
    "US"
  ],
  "currencies": [
    "USD"
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id

Returns details for the merchant account and the payment method identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```php
function getMerchantsMerchantIdPaymentMethodSettingsPaymentMethodId(
    string $merchantId,
    string $paymentMethodId
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `paymentMethodId` | `string` | Template, Required | The unique identifier of the payment method. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$paymentMethodId = 'paymentMethodId2';

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->getMerchantsMerchantIdPaymentMethodSettingsPaymentMethodId(
    $merchantId,
    $paymentMethodId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PaymentMethod1:';
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Patch-Merchants-Merchant Id-Payment Method Settings-Payment Method Id

Updates payment method details for the merchant account and the payment method identified in the path.
Depending the payment method [`type`](https://docs.adyen.com/api-explorer/Management/latest/patch/merchants/_merchantId_/paymentMethodSettings#request-type), you may need to send an additional object required for the payment method.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```php
function patchMerchantsMerchantIdPaymentMethodSettingsPaymentMethodId(
    string $merchantId,
    string $paymentMethodId,
    ?UpdatePaymentMethodInfo $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `paymentMethodId` | `string` | Template, Required | The unique identifier of the payment method. |
| `body` | [`?UpdatePaymentMethodInfo`](../../doc/models/update-payment-method-info.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PaymentMethod1`](../../doc/models/payment-method-1.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$paymentMethodId = 'paymentMethodId2';

$body = UpdatePaymentMethodInfoBuilder::init()
    ->countries(
        [
            'NL'
        ]
    )
    ->currencies(
        [
            'EUR'
        ]
    )
    ->build();

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->patchMerchantsMerchantIdPaymentMethodSettingsPaymentMethodId(
    $merchantId,
    $paymentMethodId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PaymentMethod1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "mc": {
    "transactionDescription": {
      "doingBusinessAsName": "YOUR_BUSINESS_NAME",
      "type": "fixed"
    }
  },
  "id": "PM322DZ243226G5LKBTGM7FBQ",
  "type": "mc",
  "enabled": true,
  "countries": [
    "NL"
  ],
  "currencies": [
    "EUR"
  ],
  "customRoutingFlags": []
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Post-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Add Apple Pay Domains

Adds the new domain to the list of Apple Pay domains that are registered with the merchant account and the payment method identified in the path. For more information, see [Apple Pay documentation](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in/?tab=adyen-certificate-live_1#going-live).

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read and write

```php
function postMerchantsMerchantIdPaymentMethodSettingsPaymentMethodIdAddApplePayDomains(
    string $merchantId,
    string $paymentMethodId,
    ?ApplePayInfo $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `paymentMethodId` | `string` | Template, Required | The unique identifier of the payment method. |
| `body` | [`?ApplePayInfo`](../../doc/models/apple-pay-info.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```php
$merchantId = 'merchantId6';

$paymentMethodId = 'paymentMethodId2';

$body = ApplePayInfoBuilder::init(
    [
        'https://example.com'
    ]
)->build();

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->postMerchantsMerchantIdPaymentMethodSettingsPaymentMethodIdAddApplePayDomains(
    $merchantId,
    $paymentMethodId,
    $body
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
| 429 | - | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`RestServiceErrorException`](../../doc/models/rest-service-error-exception.md) |


# Get-Merchants-Merchant Id-Payment Method Settings-Payment Method Id-Get Apple Pay Domains

Returns all Apple Pay domains that are registered with the merchant account and the payment method identified in the path. For more information, see [Apple Pay documentation](https://docs.adyen.com/payment-methods/apple-pay/enable-apple-pay#register-merchant-domain).

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Payment methods read

```php
function getMerchantsMerchantIdPaymentMethodSettingsPaymentMethodIdGetApplePayDomains(
    string $merchantId,
    string $paymentMethodId
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `paymentMethodId` | `string` | Template, Required | The unique identifier of the payment method. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ApplePayInfo`](../../doc/models/apple-pay-info.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$paymentMethodId = 'paymentMethodId2';

$paymentMethodsMerchantLevelApi = $client->getPaymentMethodsMerchantLevelApi();
$apiResponse = $paymentMethodsMerchantLevelApi->getMerchantsMerchantIdPaymentMethodSettingsPaymentMethodIdGetApplePayDomains(
    $merchantId,
    $paymentMethodId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ApplePayInfo:';
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

