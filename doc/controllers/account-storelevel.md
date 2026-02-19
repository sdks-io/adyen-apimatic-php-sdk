# Account-Storelevel

```php
$accountStorelevelApi = $client->getAccountStorelevelApi();
```

## Class Name

`AccountStorelevelApi`

## Methods

* [Get-Merchants-Merchant Id-Stores](../../doc/controllers/account-storelevel.md#get-merchants-merchant-id-stores)
* [Post-Merchants-Merchant Id-Stores](../../doc/controllers/account-storelevel.md#post-merchants-merchant-id-stores)
* [Get-Merchants-Merchant Id-Stores-Store Id](../../doc/controllers/account-storelevel.md#get-merchants-merchant-id-stores-store-id)
* [Patch-Merchants-Merchant Id-Stores-Store Id](../../doc/controllers/account-storelevel.md#patch-merchants-merchant-id-stores-store-id)
* [Get-Stores](../../doc/controllers/account-storelevel.md#get-stores)
* [Post-Stores](../../doc/controllers/account-storelevel.md#post-stores)
* [Get-Stores-Store Id](../../doc/controllers/account-storelevel.md#get-stores-store-id)
* [Patch-Stores-Store Id](../../doc/controllers/account-storelevel.md#patch-stores-store-id)


# Get-Merchants-Merchant Id-Stores

Returns a list of stores for the merchant account identified in the path. The list is grouped into pages as defined by the query parameters.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getMerchantsMerchantIdStores(
    string $merchantId,
    ?int $pageNumber = null,
    ?int $pageSize = null,
    ?string $reference = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `reference` | `?string` | Query, Optional | The reference of the store. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListStoresResponse`](../../doc/models/list-stores-response.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->getMerchantsMerchantIdStores($merchantId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListStoresResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "_links": {
    "first": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    },
    "last": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "next": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "self": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    }
  },
  "itemsTotal": 2,
  "pagesTotal": 1,
  "data": [
    {
      "id": "ST322LJ223223K5F4SQNR9XL5",
      "address": {
        "city": "Springfield",
        "country": "US",
        "line1": "200 Main Street",
        "line2": "Building 5A",
        "line3": "Suite 3",
        "postalCode": "20250",
        "stateOrProvince": "NY"
      },
      "description": "City centre store",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+13123456789",
      "reference": "Springfield Shop",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
        }
      }
    },
    {
      "id": "ST322LJ223223K5F4SQNR9XL6",
      "address": {
        "city": "North Madison",
        "country": "US",
        "line1": "1492 Townline Road",
        "line2": "Rowland Business Park",
        "postalCode": "20577",
        "stateOrProvince": "NY"
      },
      "description": "West location",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1211992213193020",
      "reference": "Second Madison store",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL6"
        }
      }
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


# Post-Merchants-Merchant Id-Stores

Creates a store for the merchant account identified in the path.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function postMerchantsMerchantIdStores(string $merchantId, ?StoreCreationRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `body` | [`?StoreCreationRequest`](../../doc/models/store-creation-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$body = StoreCreationRequestBuilder::init(
    StoreLocation1Builder::init(
        'US'
    )
        ->city('Springfield')
        ->line1('200 Main Street')
        ->line2('Building 5A')
        ->line3('Suite 3')
        ->postalCode('20250')
        ->stateOrProvince('NY')
        ->build(),
    'City centre store',
    '13123456789',
    'Springfield Shop'
)
    ->reference('Spring_store_2')
    ->build();

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->postMerchantsMerchantIdStores(
    $merchantId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20250"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
    }
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


# Get-Merchants-Merchant Id-Stores-Store Id

Returns the details of the store identified in the path.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getMerchantsMerchantIdStoresStoreId(string $merchantId, string $storeId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$storeId = 'storeId6';

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->getMerchantsMerchantIdStoresStoreId(
    $merchantId,
    $storeId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "address": {
    "city": "Springfield",
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "postalCode": "20250",
    "stateOrProvince": "NY"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "phoneNumber": "+13123456789",
  "reference": "Springfield Shop",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
    }
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


# Patch-Merchants-Merchant Id-Stores-Store Id

Updates the store identified in the path. You can only update some store parameters.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function patchMerchantsMerchantIdStoresStoreId(
    string $merchantId,
    string $storeId,
    ?UpdateStoreRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchantId` | `string` | Template, Required | The unique identifier of the merchant account. |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |
| `body` | [`?UpdateStoreRequest`](../../doc/models/update-store-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$merchantId = 'merchantId6';

$storeId = 'storeId6';

$body = UpdateStoreRequestBuilder::init()
    ->address(
        UpdatableAddress1Builder::init()
            ->line1('1776 West Pinewood Avenue')
            ->line2('Heartland Building')
            ->line3('')
            ->postalCode('20251')
            ->build()
    )
    ->build();

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->patchMerchantsMerchantIdStoresStoreId(
    $merchantId,
    $storeId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "1776 West Pinewood Avenue",
    "line2": "Heartland Building",
    "line3": "",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20251"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
    }
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


# Get-Stores

Returns a list of stores. The list is grouped into pages as defined by the query parameters.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getStores(
    ?int $pageNumber = null,
    ?int $pageSize = null,
    ?string $reference = null,
    ?string $merchantId = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |
| `reference` | `?string` | Query, Optional | The reference of the store. |
| `merchantId` | `?string` | Query, Optional | The unique identifier of the merchant account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListStoresResponse`](../../doc/models/list-stores-response.md).

## Example Usage

```php
$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->getStores();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListStoresResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "_links": {
    "first": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    },
    "last": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "next": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=2&pageSize=1"
    },
    "self": {
      "href": "https://management-test.adyen.com/v1/merchants/YOUR_MERCHANT_ACCOUNT_ID/stores?pageNumber=1&pageSize=1"
    }
  },
  "itemsTotal": 2,
  "pagesTotal": 1,
  "data": [
    {
      "id": "ST322LJ223223K5F4SQNR9XL5",
      "address": {
        "city": "Springfield",
        "country": "US",
        "line1": "200 Main Street",
        "line2": "Building 5A",
        "line3": "Suite 3",
        "postalCode": "20250",
        "stateOrProvince": "NY"
      },
      "description": "City centre store",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1312345678",
      "reference": "Springfield Shop",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
        }
      }
    },
    {
      "id": "ST322LJ223223K5F4SQNR9XL6",
      "address": {
        "city": "North Madison",
        "country": "US",
        "line1": "1492 Townline Road",
        "line2": "Rowland Business Park",
        "postalCode": "20577",
        "stateOrProvince": "NY"
      },
      "description": "West location",
      "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
      "phoneNumber": "+1211992213193020",
      "reference": "Second Madison store",
      "status": "active",
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL6"
        }
      }
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


# Post-Stores

Creates a store for the merchant account specified in the request.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function postStores(?StoreCreationWithMerchantCodeRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?StoreCreationWithMerchantCodeRequest`](../../doc/models/store-creation-with-merchant-code-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$body = StoreCreationWithMerchantCodeRequestBuilder::init(
    StoreLocation1Builder::init(
        'US'
    )
        ->city('Springfield')
        ->line1('200 Main Street')
        ->line2('Building 5A')
        ->line3('Suite 3')
        ->postalCode('20250')
        ->stateOrProvince('NY')
        ->build(),
    'City centre store',
    'YOUR_MERCHANT_ACCOUNT_ID',
    '+13123456789',
    'Springfield Shop'
)
    ->reference('Spring_store_2')
    ->build();

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->postStores($body);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20250"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
    }
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


# Get-Stores-Store Id

Returns the details of the store identified in the path.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read
* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getStoresStoreId(string $storeId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$storeId = 'storeId6';

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->getStoresStoreId($storeId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "ST322LJ223223K5F4SQNR9XL5",
  "address": {
    "city": "Springfield",
    "country": "US",
    "line1": "200 Main Street",
    "line2": "Building 5A",
    "line3": "Suite 3",
    "postalCode": "20250",
    "stateOrProvince": "NY"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "phoneNumber": "+13123456789",
  "reference": "Springfield Shop",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/ST322LJ223223K5F4SQNR9XL5"
    }
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


# Patch-Stores-Store Id

Updates the store identified in the path.
You can only update some store parameters.

To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Stores read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function patchStoresStoreId(string $storeId, ?UpdateStoreRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `storeId` | `string` | Template, Required | The unique identifier of the store. |
| `body` | [`?UpdateStoreRequest`](../../doc/models/update-store-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Store`](../../doc/models/store.md).

## Example Usage

```php
$storeId = 'storeId6';

$body = UpdateStoreRequestBuilder::init()
    ->address(
        UpdatableAddress1Builder::init()
            ->line1('1776 West Pinewood Avenue')
            ->line2('Heartland Building')
            ->line3('')
            ->postalCode('20251')
            ->build()
    )
    ->build();

$accountStoreLevelApi = $client->getAccountStoreLevelApi();
$apiResponse = $accountStoreLevelApi->patchStoresStoreId(
    $storeId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Store:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "YOUR_STORE_ID",
  "address": {
    "country": "US",
    "line1": "1776 West Pinewood Avenue",
    "line2": "Heartland Building",
    "line3": "",
    "city": "Springfield",
    "stateOrProvince": "NY",
    "postalCode": "20251"
  },
  "description": "City centre store",
  "merchantId": "YOUR_MERCHANT_ACCOUNT_ID",
  "shopperStatement": "Springfield Shop",
  "phoneNumber": "+13123456789",
  "reference": "Spring_store_2",
  "status": "active",
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/stores/YOUR_STORE_ID"
    }
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

