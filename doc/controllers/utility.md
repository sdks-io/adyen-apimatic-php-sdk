# Utility

```php
$utilityApi = $client->getUtilityApi();
```

## Class Name

`UtilityApi`

## Methods

* [Get Apple Pay Session](../../doc/controllers/utility.md#get-apple-pay-session)
* [Generate Origin Keys](../../doc/controllers/utility.md#generate-origin-keys)
* [Update Pay Pal Order](../../doc/controllers/utility.md#update-pay-pal-order)
* [Validate Shopper Id](../../doc/controllers/utility.md#validate-shopper-id)


# Get Apple Pay Session

You need to use this endpoint if you have an API-only integration with Apple Pay which uses Adyen's Apple Pay certificate.

The endpoint returns the Apple Pay session data which you need to complete the [Apple Pay session validation](https://docs.adyen.com/payment-methods/apple-pay/api-only?tab=adyen-certificate-validation_1#complete-apple-pay-session-validation).

```php
function getApplePaySession(?string $idempotencyKey = null, ?ApplePaySessionRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotencyKey` | `?string` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`?ApplePaySessionRequest`](../../doc/models/apple-pay-session-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ApplePaySessionResponse`](../../doc/models/apple-pay-session-response.md).

## Example Usage

```php
$body = ApplePaySessionRequestBuilder::init(
    'YOUR_MERCHANT_NAME',
    'YOUR_DOMAIN_NAME',
    'YOUR_MERCHANT_ID'
)->build();

$utilityApi = $client->getUtilityApi();
$apiResponse = $utilityApi->getApplePaySession(
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ApplePaySessionResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "data": "eyJ2Z..."
}
```


# Generate Origin Keys

**This endpoint is deprecated.**

This operation takes the origin domains and returns a JSON object containing the corresponding origin keys for the domains.

> If you're still using origin key for your Web Drop-in or Components integration, we recommend [switching to client key](https://docs.adyen.com/development-resources/client-side-authentication/migrate-from-origin-key-to-client-key). This allows you to use a single key for all origins, add or remove origins without generating a new key, and detect the card type from the number entered in your payment form.

```php
function generateOriginKeys(?string $idempotencyKey = null, ?UtilityRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotencyKey` | `?string` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`?UtilityRequest`](../../doc/models/utility-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UtilityResponse`](../../doc/models/utility-response.md).

## Example Usage

```php
$body = UtilityRequestBuilder::init(
    [
        'https://www.your-domain1.com',
        'https://www.your-domain2.com',
        'https://www.your-domain3.com'
    ]
)->build();

$utilityApi = $client->getUtilityApi();
$apiResponse = $utilityApi->generateOriginKeys(
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UtilityResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "originKeys": {
    "https://www.your-domain1.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4xLmNvbQ.pvbYlrXz0ICP4kwMJXDGDLVMqALhwXr1MSRjT-fkhvw",
    "https://www.your-domain3.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4zLmNvbQ.FrTpVz7_RzAywKasM0kXCRoMfoMkKIKaxjFymRGORIc",
    "https://www.your-domain2.com": "pub.v2.8116178901076090.aHR0cHM6Ly93d3cueW91ci1kb21haW4yLmNvbQ.LdN9kvJ35fYFFiBSJA4idMnwwxJ5_yXpeNS__Ap5wkg"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |


# Update Pay Pal Order

Updates the order for PayPal Express Checkout. This can be used to update the PayPal lightbox with an updated amount and delivery methods based on the delivery address.

```php
function updatePayPalOrder(?string $idempotencyKey = null, ?PaypalUpdateOrderRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotencyKey` | `?string` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`?PaypalUpdateOrderRequest`](../../doc/models/paypal-update-order-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PaypalUpdateOrderResponse`](../../doc/models/paypal-update-order-response.md).

## Example Usage

```php
$body = PaypalUpdateOrderRequestBuilder::init()
    ->amount(
        Amount43Builder::init(
            'EUR',
            12000
        )->build()
    )
    ->deliveryMethods(
        [
            DeliveryMethodBuilder::init()
                ->amount(
                    Amount23Builder::init(
                        'EUR',
                        1000
                    )->build()
                )
                ->description('Express Shipping')
                ->reference('1')
                ->selected(true)
                ->type(Type18::SHIPPING)
                ->build(),
            DeliveryMethodBuilder::init()
                ->amount(
                    Amount23Builder::init(
                        'EUR',
                        500
                    )->build()
                )
                ->description('Standard Ground')
                ->reference('2')
                ->selected(false)
                ->type(Type18::SHIPPING)
                ->build()
        ]
    )
    ->paymentData('po7XZ...')
    ->pspReference('DZ4DPSHB4WD2WN82')
    ->build();

$utilityApi = $client->getUtilityApi();
$apiResponse = $utilityApi->updatePayPalOrder(
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PaypalUpdateOrderResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "paymentData": "po7XZ...",
  "status": "success"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 401 | Unauthorized - authentication required. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`ServiceErrorException`](../../doc/models/service-error-exception.md) |


# Validate Shopper Id

Validates the shopperId.

:information_source: **Note** This endpoint does not require authentication.

```php
function validateShopperId(ValidateShopperIdRequest $body): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`ValidateShopperIdRequest`](../../doc/models/validate-shopper-id-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ValidateShopperIdResponse`](../../doc/models/validate-shopper-id-response.md).

## Example Usage

```php
$body = ValidateShopperIdRequestBuilder::init(
    'merchantAccount2',
    ShopperIdPaymentMethod1Builder::init()
        ->type('ShopperIdPaymentMethod1')
        ->build()
)->build();

$utilityApi = $client->getUtilityApi();
$apiResponse = $utilityApi->validateShopperId($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ValidateShopperIdResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request - a problem reading or understanding the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 401 | Unauthorized - authentication required. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 403 | Forbidden - insufficient permissions to process the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 422 | Unprocessable Entity - a request validation error. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |
| 500 | Internal Server Error - the server could not process the request. | [`DefaultErrorResponseEntityException`](../../doc/models/default-error-response-entity-exception.md) |

