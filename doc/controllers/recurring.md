# Recurring

```php
$recurringApi = $client->getRecurringApi();
```

## Class Name

`RecurringApi`

## Methods

* [Post-Forward](../../doc/controllers/recurring.md#post-forward)
* [Get-Stored Payment Methods](../../doc/controllers/recurring.md#get-stored-payment-methods)
* [Post-Stored Payment Methods](../../doc/controllers/recurring.md#post-stored-payment-methods)
* [Delete-Stored Payment Methods-Stored Payment Method Id](../../doc/controllers/recurring.md#delete-stored-payment-methods-stored-payment-method-id)


# Post-Forward

Forwards the payment details you stored with Adyen to a third-party that you specify and returns the response from the third-party. Supports forwarding stored card details or [network tokens](https://docs.adyen.com/online-payments/network-tokenization). For more information, see [Forward stored payment details](https://docs.adyen.com/online-payments/tokenization/forward-payment-details).

```php
function postForward(?string $idempotencyKey = null, ?CheckoutForwardRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotencyKey` | `?string` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`?CheckoutForwardRequest`](../../doc/models/checkout-forward-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CheckoutForwardResponse`](../../doc/models/checkout-forward-response.md).

## Example Usage

```php
$body = CheckoutForwardRequestBuilder::init(
    'http://thirdparty.example.com',
    'YOUR_MERCHANT_ACCOUNT',
    CheckoutOutgoingForwardRequest2Builder::init(
        '{"amount":{"value":100,"currency":"USD"},"paymentMethod":{"creditCard":{"holderName":"{{holderName}}","number":"{{number}}","expiryMonth":"{{expiryMonth}}","expiryYear":"{{expiryYear}}"}}}',
        HttpMethod::POST
    )
        ->credentials('YOUR_CREDENTIALS_FOR_THE_THIRD_PARTY')
        ->headers(
            [
                'Authorization' => 'Basic {{credentials}}'
            ]
        )
        ->urlSuffix('/payments')
        ->build(),
    'YOUR_SHOPPER_REFERENCE'
)
    ->storedPaymentMethodId('M5N7TQ4TG5PFWR50')
    ->build();

$recurringApi = $client->getRecurringApi();
$apiResponse = $recurringApi->postForward(
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CheckoutForwardResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "storedPaymentMethodId": "M5N7TQ4TG5PFWR50",
  "pspReference": "XB7XNCQ8HXSKGK82",
  "response": {
    "status": 200,
    "headers": {
      "thirdparty-version": "2023-10-16"
    },
    "body": "{\"success\": \"ok\",\"data\": {\"tokenizeCreditCard\": {\"paymentMethod\": {\"id\": \"PAYMENT_METHOD_ID\"}}}}"
  }
}
```


# Get-Stored Payment Methods

Lists the tokens for stored payment details for the shopper identified in the path, if there are any available. The token ID can be used with payment requests for the shopper's payment. A summary of the stored details is included.

```php
function getStoredPaymentMethods(?string $shopperReference = null, ?string $merchantAccount = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `shopperReference` | `?string` | Query, Optional | Your reference to uniquely identify this shopper, for example user ID or account ID. Minimum length: 3 characters.<br><br>> Your reference must not include personally identifiable information (PII), for example name or email address. |
| `merchantAccount` | `?string` | Query, Optional | Your merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListStoredPaymentMethodsResponse`](../../doc/models/list-stored-payment-methods-response.md).

## Example Usage

```php
$recurringApi = $client->getRecurringApi();
$apiResponse = $recurringApi->getStoredPaymentMethods();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListStoredPaymentMethodsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "merchantAccount": "YOUR_MERCHANT_ACCOUNT",
  "shopperReference": "YOUR_SHOPPER_REFERENCE",
  "storedPaymentMethods": [
    {
      "brand": "visa",
      "expiryMonth": "10",
      "expiryYear": "30",
      "holderName": "John Smith",
      "id": "7219687191761347",
      "issuerName": "ISSUER_NAME",
      "lastFour": "1111",
      "name": "VISA",
      "shopperEmail": "john.smith@example.com",
      "shopperReference": "YOUR_SHOPPER_REFERENCE",
      "supportedRecurringProcessingModels": [
        "CardOnFile",
        "Subscription",
        "UnscheduledCardOnFile"
      ],
      "type": "scheme"
    }
  ]
}
```


# Post-Stored Payment Methods

Creates a token to store the shopper's payment details. This token can be used for the shopper's future payments.

```php
function postStoredPaymentMethods(
    ?string $idempotencyKey = null,
    ?StoredPaymentMethodRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotencyKey` | `?string` | Header, Optional | A unique identifier for the message with a maximum of 64 characters (we recommend a UUID). |
| `body` | [`?StoredPaymentMethodRequest`](../../doc/models/stored-payment-method-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`StoredPaymentMethodResource`](../../doc/models/stored-payment-method-resource.md).

## Example Usage

```php
$body = StoredPaymentMethodRequestBuilder::init(
    'YOUR_MERCHANT_ACCOUNT',
    PaymentMethodToStore1Builder::init()
        ->encryptedCardNumber('test_4111111111111111')
        ->encryptedExpiryMonth('test_03')
        ->encryptedExpiryYear('test_2030')
        ->encryptedSecurityCode('test_737')
        ->holderName('John Smith')
        ->type('scheme')
        ->build(),
    RecurringProcessingModel1::SUBSCRIPTION,
    'YOUR_SHOPPER_REFERENCE'
)
    ->shopperEmail('s.hopper@test.com')
    ->shopperIp('192.0.2.1')
    ->build();

$recurringApi = $client->getRecurringApi();
$apiResponse = $recurringApi->postStoredPaymentMethods(
    null,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'StoredPaymentMethodResource:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "expiryMonth": "03",
  "expiryYear": "2030",
  "holderName": "John Smith",
  "id": "KHQC5N7G84BLNK43",
  "lastFour": "1111",
  "shopperReference": "YOUR_SHOPPER_REFERENCE",
  "type": "scheme"
}
```


# Delete-Stored Payment Methods-Stored Payment Method Id

Deletes the token identified in the path. The token can no longer be used with payment requests.

```php
function deleteStoredPaymentMethodsStoredPaymentMethodId(
    string $storedPaymentMethodId,
    string $shopperReference,
    string $merchantAccount
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storedPaymentMethodId` | `string` | Template, Required | The unique identifier of the token. |
| `shopperReference` | `string` | Query, Required | Your reference to uniquely identify this shopper, for example user ID or account ID. Minimum length: 3 characters.<br><br>> Your reference must not include personally identifiable information (PII), for example name or email address. |
| `merchantAccount` | `string` | Query, Required | Your merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```php
$storedPaymentMethodId = 'storedPaymentMethodId4';

$shopperReference = 'shopperReference8';

$merchantAccount = 'merchantAccount8';

$recurringApi = $client->getRecurringApi();
$apiResponse = $recurringApi->deleteStoredPaymentMethodsStoredPaymentMethodId(
    $storedPaymentMethodId,
    $shopperReference,
    $merchantAccount
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

