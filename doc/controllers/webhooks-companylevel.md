# Webhooks-Companylevel

```php
$webhooksCompanylevelApi = $client->getWebhooksCompanylevelApi();
```

## Class Name

`WebhooksCompanylevelApi`

## Methods

* [List Company Webhooks](../../doc/controllers/webhooks-companylevel.md#list-company-webhooks)
* [Create Company Webhook](../../doc/controllers/webhooks-companylevel.md#create-company-webhook)
* [Delete Company Webhook](../../doc/controllers/webhooks-companylevel.md#delete-company-webhook)
* [Get Company Webhook](../../doc/controllers/webhooks-companylevel.md#get-company-webhook)
* [Update Company Webhook](../../doc/controllers/webhooks-companylevel.md#update-company-webhook)
* [Generate Company Webhook Hmac](../../doc/controllers/webhooks-companylevel.md#generate-company-webhook-hmac)
* [Test Company Webhook](../../doc/controllers/webhooks-companylevel.md#test-company-webhook)


# List Company Webhooks

Lists all webhook configurations for the company account.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read
* Management API—Webhooks read and write

```php
function listCompanyWebhooks(string $companyId, ?int $pageNumber = null, ?int $pageSize = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | Unique identifier of the [company account](https://docs.adyen.com/account/account-structure#company-account). |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 10 items on a page. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListWebhooksResponse`](../../doc/models/list-webhooks-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->listCompanyWebhooks($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListWebhooksResponse:';
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
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks?pageNumber=1&pageSize=10"
    },
    "last": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks?pageNumber=1&pageSize=10"
    },
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks?pageNumber=1&pageSize=10"
    }
  },
  "itemsTotal": 1,
  "pagesTotal": 1,
  "data": [
    {
      "id": "S2-4A3B33202A46",
      "type": "standard",
      "url": "YOUR_WEBHOOK_URL",
      "description": "Webhook for YOUR_COMPANY_ACCOUNT - YOUR_COMPANY_CODE",
      "filterMerchantAccountType": "allAccounts",
      "username": "adyen",
      "hasPassword": true,
      "active": true,
      "hasError": false,
      "communicationFormat": "json",
      "acceptsExpiredCertificate": false,
      "acceptsSelfSignedCertificate": false,
      "acceptsUntrustedRootCertificate": false,
      "populateSoapActionHeader": false,
      "additionalSettings": {
        "properties": {
          "includePosTerminalInfo": false,
          "includeARN": false,
          "includePosDetails": false,
          "includeCardInfoForRecurringContractNotification": false,
          "includeRiskData": false,
          "includeRiskExperimentReference": false,
          "includeSoapSecurityHeader": false,
          "includeContactlessWalletTokenInformation": false,
          "includeAcquirerReference": false,
          "includeRiskProfileReference": false,
          "includeOriginalMerchantReferenceCancelOrRefundNotification": false,
          "includeNfcTokenInformation": false,
          "includeSubvariant": false,
          "includeThreeDSVersion": false,
          "includeInstallmentsInfo": false,
          "includeAliasInfo": false,
          "includeShopperCountry": false,
          "includeRawThreeDSecureResult": false,
          "includeAirlineData": false,
          "includeGrossCurrencyChargebackDetails": false,
          "includeThreeDSecureResult": false,
          "includeMetadataIn3DSecurePaymentNotification": false,
          "includeOriginalReferenceForChargebackReversed": false,
          "addAcquirerResult": false,
          "includeDeliveryAddress": false,
          "includeRetryAttempts": false,
          "includeExtraCosts": false,
          "includeCardHolderName": false,
          "includeShopperDetail": false,
          "includeBankAccountDetails": false,
          "includeMandateDetails": false,
          "includeAuthAmountForDynamicZeroAuth": false,
          "includeIssuerCountry": false,
          "includeAcquirerErrorDetails": false,
          "includeCoBrandedWith": false,
          "includeShopperInteraction": false,
          "includeDeviceAndBrowserInfo": false,
          "addRawAcquirerResult": false,
          "includeCardBin": false,
          "includeFundingSource": false,
          "includeThreeDS2ChallengeInformation": false,
          "includeRiskProfile": false,
          "includeRealtimeAccountUpdaterStatus": false,
          "includeDunningProjectData": false,
          "includePaymentResultInOrderClosedNotification": false,
          "includeCardBinDetails": false,
          "includeNotesInManualReviewNotifications": false,
          "includeZeroAuthFlag": false,
          "addCaptureReferenceToDisputeNotification": false,
          "includePayPalDetails": false,
          "includeRawThreeDSecureDetailsResult": false,
          "includeBankVerificationResults": false,
          "includeCaptureDelayHours": false,
          "addPaymentAccountReference": false,
          "includePayULatamDetails": false,
          "includeStore": false,
          "returnAvsData": false,
          "includeWeChatPayOpenid": false,
          "includeUpiVpa": false,
          "includeUpiMetadata": false,
          "includeCustomRoutingFlagging": false,
          "includeTokenisedPaymentMetaData": false
        }
      },
      "_links": {
        "self": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46"
        },
        "company": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT"
        },
        "generateHmac": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/generateHmac"
        },
        "testWebhook": {
          "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/test"
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


# Create Company Webhook

Subscribe to receive webhook notifications about events related to your company account. You can add basic authentication to make sure the data is secure.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read and write

```php
function createCompanyWebhook(string $companyId, ?CreateCompanyWebhookRequest $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | Unique identifier of the [company account](https://docs.adyen.com/account/account-structure#company-account). |
| `body` | [`?CreateCompanyWebhookRequest`](../../doc/models/create-company-webhook-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Webhook`](../../doc/models/webhook.md).

## Example Usage

```php
$companyId = 'companyId0';

$body = CreateCompanyWebhookRequestBuilder::init(
    true,
    CommunicationFormat::SOAP,
    FilterMerchantAccountType::INCLUDEACCOUNTS,
    [
        'YOUR_MERCHANT_ACCOUNT'
    ],
    'standard',
    'YOUR_WEBHOOK_URL'
)
    ->acceptsExpiredCertificate(false)
    ->acceptsSelfSignedCertificate(true)
    ->acceptsUntrustedRootCertificate(true)
    ->password('YOUR_PASSWORD')
    ->populateSoapActionHeader(false)
    ->username('YOUR_USER')
    ->build();

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->createCompanyWebhook(
    $companyId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Webhook:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "S2-6933523D2772",
  "type": "standard",
  "url": "YOUR_WEBHOOK_URL",
  "description": "Webhook for YOUR_COMPANY_ACCOUNT - YOUR_COMPANY_CODE",
  "filterMerchantAccountType": "includeAccounts",
  "filterMerchantAccounts": [
    "YOUR_MERCHANT_ACCOUNT"
  ],
  "username": "myuser",
  "hasPassword": true,
  "active": true,
  "hasError": false,
  "communicationFormat": "soap",
  "acceptsExpiredCertificate": false,
  "acceptsSelfSignedCertificate": true,
  "acceptsUntrustedRootCertificate": true,
  "certificateAlias": "signed-test.adyen.com_2024",
  "populateSoapActionHeader": false,
  "additionalSettings": {
    "properties": {
      "includePosTerminalInfo": false,
      "includeARN": false,
      "includePosDetails": false,
      "includeCardInfoForRecurringContractNotification": false,
      "includeRiskData": false,
      "includeRiskExperimentReference": false,
      "includeSoapSecurityHeader": false,
      "includeContactlessWalletTokenInformation": false,
      "includeAcquirerReference": false,
      "includeRiskProfileReference": false,
      "includeOriginalMerchantReferenceCancelOrRefundNotification": false,
      "includeNfcTokenInformation": false,
      "includeSubvariant": false,
      "includeThreeDSVersion": false,
      "includeInstallmentsInfo": false,
      "includeAliasInfo": false,
      "includeShopperCountry": false,
      "includeRawThreeDSecureResult": false,
      "includeAirlineData": false,
      "includeGrossCurrencyChargebackDetails": false,
      "includeThreeDSecureResult": false,
      "includeMetadataIn3DSecurePaymentNotification": false,
      "includeOriginalReferenceForChargebackReversed": false,
      "addAcquirerResult": false,
      "includeDeliveryAddress": false,
      "includeRetryAttempts": false,
      "includeExtraCosts": false,
      "includeCardHolderName": false,
      "includeShopperDetail": false,
      "includeBankAccountDetails": false,
      "includeMandateDetails": false,
      "includeAuthAmountForDynamicZeroAuth": false,
      "includeIssuerCountry": false,
      "includeAcquirerErrorDetails": false,
      "includeCoBrandedWith": false,
      "includeShopperInteraction": false,
      "includeDeviceAndBrowserInfo": false,
      "addRawAcquirerResult": false,
      "includeCardBin": false,
      "includeFundingSource": false,
      "includeThreeDS2ChallengeInformation": false,
      "includeRiskProfile": false,
      "includeRealtimeAccountUpdaterStatus": false,
      "includeDunningProjectData": false,
      "includePaymentResultInOrderClosedNotification": false,
      "includeCardBinDetails": false,
      "includeNotesInManualReviewNotifications": false,
      "includeZeroAuthFlag": false,
      "addCaptureReferenceToDisputeNotification": false,
      "includePayPalDetails": false,
      "includeRawThreeDSecureDetailsResult": false,
      "includeBankVerificationResults": false,
      "includeCaptureDelayHours": false,
      "addPaymentAccountReference": false,
      "includePayULatamDetails": false,
      "includeStore": false,
      "returnAvsData": false,
      "includeWeChatPayOpenid": false,
      "includeUpiVpa": false,
      "includeUpiMetadata": false,
      "includeCustomRoutingFlagging": false,
      "includeTokenisedPaymentMetaData": false
    }
  },
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-6933523D2772"
    },
    "company": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT"
    },
    "generateHmac": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-6933523D2772/generateHmac"
    },
    "testWebhook": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-6933523D2772/test"
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


# Delete Company Webhook

Remove the configuration for the webhook identified in the path.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read and write

```php
function deleteCompanyWebhook(string $companyId, string $webhookId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `webhookId` | `string` | Template, Required | Unique identifier of the webhook configuration. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```php
$companyId = 'companyId0';

$webhookId = 'webhookId6';

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->deleteCompanyWebhook(
    $companyId,
    $webhookId
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


# Get Company Webhook

Returns the configuration for the webhook identified in the path.

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read
* Management API—Webhooks read and write

```php
function getCompanyWebhook(string $companyId, string $webhookId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | Unique identifier of the [company account](https://docs.adyen.com/account/account-structure#company-account). |
| `webhookId` | `string` | Template, Required | Unique identifier of the webhook configuration. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Webhook`](../../doc/models/webhook.md).

## Example Usage

```php
$companyId = 'companyId0';

$webhookId = 'webhookId6';

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->getCompanyWebhook(
    $companyId,
    $webhookId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Webhook:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "S2-4A3B33202A46",
  "type": "standard",
  "url": "YOUR_WEBHOOK_URL",
  "description": "Webhook for YOUR_COMPANY_ACCOUNT - YOUR_COMPANY_CODE",
  "filterMerchantAccountType": "allAccounts",
  "username": "adyen",
  "hasPassword": true,
  "active": true,
  "hasError": false,
  "communicationFormat": "json",
  "acceptsExpiredCertificate": false,
  "acceptsSelfSignedCertificate": false,
  "acceptsUntrustedRootCertificate": false,
  "populateSoapActionHeader": false,
  "additionalSettings": {
    "properties": {
      "includePosTerminalInfo": false,
      "includeARN": false,
      "includePosDetails": false,
      "includeCardInfoForRecurringContractNotification": false,
      "includeRiskData": false,
      "includeRiskExperimentReference": false,
      "includeSoapSecurityHeader": false,
      "includeContactlessWalletTokenInformation": false,
      "includeAcquirerReference": false,
      "includeRiskProfileReference": false,
      "includeOriginalMerchantReferenceCancelOrRefundNotification": false,
      "includeNfcTokenInformation": false,
      "includeSubvariant": false,
      "includeThreeDSVersion": false,
      "includeInstallmentsInfo": false,
      "includeAliasInfo": false,
      "includeShopperCountry": false,
      "includeRawThreeDSecureResult": false,
      "includeAirlineData": false,
      "includeGrossCurrencyChargebackDetails": false,
      "includeThreeDSecureResult": false,
      "includeMetadataIn3DSecurePaymentNotification": false,
      "includeOriginalReferenceForChargebackReversed": false,
      "addAcquirerResult": false,
      "includeDeliveryAddress": false,
      "includeRetryAttempts": false,
      "includeExtraCosts": false,
      "includeCardHolderName": false,
      "includeShopperDetail": false,
      "includeBankAccountDetails": false,
      "includeMandateDetails": false,
      "includeAuthAmountForDynamicZeroAuth": false,
      "includeIssuerCountry": false,
      "includeAcquirerErrorDetails": false,
      "includeCoBrandedWith": false,
      "includeShopperInteraction": false,
      "includeDeviceAndBrowserInfo": false,
      "addRawAcquirerResult": false,
      "includeCardBin": false,
      "includeFundingSource": false,
      "includeThreeDS2ChallengeInformation": false,
      "includeRiskProfile": false,
      "includeRealtimeAccountUpdaterStatus": false,
      "includeDunningProjectData": false,
      "includePaymentResultInOrderClosedNotification": false,
      "includeCardBinDetails": false,
      "includeNotesInManualReviewNotifications": false,
      "includeZeroAuthFlag": false,
      "addCaptureReferenceToDisputeNotification": false,
      "includePayPalDetails": false,
      "includeRawThreeDSecureDetailsResult": false,
      "includeBankVerificationResults": false,
      "includeCaptureDelayHours": false,
      "addPaymentAccountReference": false,
      "includePayULatamDetails": false,
      "includeStore": false,
      "returnAvsData": false,
      "includeWeChatPayOpenid": false,
      "includeUpiVpa": false,
      "includeUpiMetadata": false,
      "includeCustomRoutingFlagging": false,
      "includeTokenisedPaymentMetaData": false
    }
  },
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46"
    },
    "company": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT"
    },
    "generateHmac": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/generateHmac"
    },
    "testWebhook": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/test"
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


# Update Company Webhook

Make changes to the configuration of the webhook identified in the path. The request contains the new values you want to have in the webhook configuration. The response contains the full configuration for the webhook, which includes the new values from the request.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read and write

```php
function updateCompanyWebhook(
    string $companyId,
    string $webhookId,
    ?UpdateCompanyWebhookRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `webhookId` | `string` | Template, Required | Unique identifier of the webhook configuration. |
| `body` | [`?UpdateCompanyWebhookRequest`](../../doc/models/update-company-webhook-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Webhook`](../../doc/models/webhook.md).

## Example Usage

```php
$companyId = 'companyId0';

$webhookId = 'webhookId6';

$body = UpdateCompanyWebhookRequestBuilder::init()
    ->active(true)
    ->build();

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->updateCompanyWebhook(
    $companyId,
    $webhookId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Webhook:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "id": "S2-4A3B33202A46",
  "type": "standard",
  "url": "YOUR_WEBHOOK_URL",
  "description": "Webhook for YOUR_COMPANY_ACCOUNT - YOUR_COMPANY_CODE",
  "filterMerchantAccountType": "allAccounts",
  "username": "",
  "hasPassword": false,
  "active": true,
  "hasError": false,
  "communicationFormat": "json",
  "acceptsExpiredCertificate": false,
  "acceptsSelfSignedCertificate": false,
  "acceptsUntrustedRootCertificate": false,
  "populateSoapActionHeader": false,
  "additionalSettings": {
    "properties": {
      "includePosTerminalInfo": false,
      "includeARN": false,
      "includePosDetails": false,
      "includeCardInfoForRecurringContractNotification": false,
      "includeRiskData": false,
      "includeRiskExperimentReference": false,
      "includeSoapSecurityHeader": false,
      "includeContactlessWalletTokenInformation": false,
      "includeAcquirerReference": false,
      "includeRiskProfileReference": false,
      "includeOriginalMerchantReferenceCancelOrRefundNotification": false,
      "includeNfcTokenInformation": false,
      "includeSubvariant": false,
      "includeThreeDSVersion": false,
      "includeInstallmentsInfo": false,
      "includeAliasInfo": false,
      "includeShopperCountry": false,
      "includeRawThreeDSecureResult": false,
      "includeAirlineData": false,
      "includeGrossCurrencyChargebackDetails": false,
      "includeThreeDSecureResult": false,
      "includeMetadataIn3DSecurePaymentNotification": false,
      "includeOriginalReferenceForChargebackReversed": false,
      "addAcquirerResult": false,
      "includeDeliveryAddress": false,
      "includeRetryAttempts": false,
      "includeExtraCosts": false,
      "includeCardHolderName": false,
      "includeShopperDetail": false,
      "includeBankAccountDetails": false,
      "includeMandateDetails": false,
      "includeAuthAmountForDynamicZeroAuth": false,
      "includeIssuerCountry": false,
      "includeAcquirerErrorDetails": false,
      "includeCoBrandedWith": false,
      "includeShopperInteraction": false,
      "includeDeviceAndBrowserInfo": false,
      "addRawAcquirerResult": false,
      "includeCardBin": false,
      "includeFundingSource": false,
      "includeThreeDS2ChallengeInformation": false,
      "includeRiskProfile": false,
      "includeRealtimeAccountUpdaterStatus": false,
      "includeDunningProjectData": false,
      "includePaymentResultInOrderClosedNotification": false,
      "includeCardBinDetails": false,
      "includeNotesInManualReviewNotifications": false,
      "includeZeroAuthFlag": false,
      "addCaptureReferenceToDisputeNotification": false,
      "includePayPalDetails": false,
      "includeRawThreeDSecureDetailsResult": false,
      "includeBankVerificationResults": false,
      "includeCaptureDelayHours": false,
      "addPaymentAccountReference": false,
      "includePayULatamDetails": false,
      "includeStore": false,
      "returnAvsData": false,
      "includeWeChatPayOpenid": false,
      "includeUpiVpa": false,
      "includeUpiMetadata": false,
      "includeCustomRoutingFlagging": false,
      "includeTokenisedPaymentMetaData": false
    }
  },
  "_links": {
    "self": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46"
    },
    "company": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT"
    },
    "generateHmac": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/generateHmac"
    },
    "testWebhook": {
      "href": "https://management-test.adyen.com/v1/companies/YOUR_COMPANY_ACCOUNT/webhooks/S2-4A3B33202A46/test"
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


# Generate Company Webhook Hmac

Returns an [HMAC key](https://en.wikipedia.org/wiki/HMAC) for the webhook identified in the path. This key allows you to check the integrity and the origin of the notifications you receive.By creating an HMAC key, you start receiving [HMAC-signed notifications](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures#enable-hmac-signatures) from Adyen. Find out more about how to [verify HMAC signatures](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures).

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read and write

```php
function generateCompanyWebhookHmac(string $companyId, string $webhookId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `webhookId` | `string` | Template, Required | Unique identifier of the webhook configuration. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GenerateHmacKeyResponse`](../../doc/models/generate-hmac-key-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$webhookId = 'webhookId6';

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->generateCompanyWebhookHmac(
    $companyId,
    $webhookId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GenerateHmacKeyResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Example Response *(as JSON)*

```json
{
  "hmacKey": "7052E6804F0AF40DCC390464C817F4F963516FA42AC8816D518DC5D39F41E902"
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


# Test Company Webhook

Sends sample notifications to test if the webhook is set up correctly.

We send sample notifications for maximum 20 of the merchant accounts that the webhook is configured for. If the webhook is configured for more than 20 merchant accounts, use the `merchantIds` array to specify a subset of the merchant accounts for which to send test notifications.

We send four test notifications for each event code you choose. They cover success and failure scenarios for the hard-coded currencies EUR and GBP, regardless of the currencies configured in the merchant accounts. For custom notifications, we only send the specified custom notification.

The response describes the result of the test. The `status` field tells you if the test was successful or not. You can use the other response fields to troubleshoot unsuccessful tests.

To make this request, your API credential must have the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Webhooks read and write

```php
function testCompanyWebhook(
    string $companyId,
    string $webhookId,
    ?TestCompanyWebhookRequest $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `webhookId` | `string` | Template, Required | Unique identifier of the webhook configuration. |
| `body` | [`?TestCompanyWebhookRequest`](../../doc/models/test-company-webhook-request.md) | Body, Optional | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`TestWebhookResponse`](../../doc/models/test-webhook-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$webhookId = 'webhookId6';

$body = TestCompanyWebhookRequestBuilder::init()
    ->merchantIds(
        [
            'YOUR_MERCHANT_ACCOUNT'
        ]
    )
    ->types(
        [
            'AUTHORISATION'
        ]
    )
    ->build();

$webhooksCompanyLevelApi = $client->getWebhooksCompanyLevelApi();
$apiResponse = $webhooksCompanyLevelApi->testCompanyWebhook(
    $companyId,
    $webhookId,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'TestWebhookResponse:';
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
      "merchantId": "YOUR_MERCHANT_ACCOUNT_AU",
      "output": "",
      "requestSent": "{\"live\":\"false\",\"notificationItems\":[{\"NotificationRequestItem\":{\"amount\":{\"currency\":\"EUR\",\"value\":100},\"eventCode\":\"AUTHORISATION\",\"eventDate\":\"2022-05-10T16:57:19+02:00\",\"merchantAccountCode\":\"YOUR_MERCHANT_ACCOUNT_AU\",\"merchantReference\":\"6GZBF5ML\",\"operations\":[\"CANCEL\",\"CAPTURE\",\"REFUND\"],\"paymentMethod\":\"visa\",\"pspReference\":\"KDN7UP7S1JIK6XES\",\"reason\":\"\",\"success\":\"true\"}}]}",
      "responseCode": "200",
      "responseTime": "657 ms",
      "status": "success"
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

