
# Getting Started with Adyen APIs

## Introduction

Adyen Checkout API provides a simple and flexible way to initiate and authorise online payments. You can use the same integration for payments made with cards (including 3D Secure), mobile wallets, and local payment methods (for example, iDEAL and Sofort).

This API reference provides information on available endpoints and how to interact with them. To learn more about the API, visit [online payments documentation](https://docs.adyen.com/online-payments).

### Authentication

Each request to Checkout API must be signed with an API key. For this, [get your API key](https://docs.adyen.com/development-resources/api-credentials#generate-api-key) from your Customer Area, and set this key to the `X-API-Key` header value, for example:

```
curl
-H "Content-Type: application/json" \
-H "X-API-Key: YOUR_API_KEY" \
...
```

### Versioning

Checkout API supports [versioning](https://docs.adyen.com/development-resources/versioning) using a version suffix in the endpoint URL. This suffix has the following format: "vXX", where XX is the version number.

For example:

```
https://checkout-test.adyen.com/v71/payments
```

### Server-side API libraries

We provide open-source [server-side API libraries](https://docs.adyen.com/development-resources/libraries/) in several languages:

- PHP
- Java
- Node.js
- .NET
- Go
- Python
- Ruby
- Apex (beta)

See our [integration examples](https://github.com/adyen-examples#%EF%B8%8F-official-integration-examples) for example uses of the libraries.

### Developer resources

Checkout API is available through a Postman collection. Click the button below to create a fork, then set the environment variables at **Environments**&nbsp;>&nbsp;**Adyen&nbsp;APIs**.

[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/25716737-46ad970e-dc9e-4246-bac2-769c6083e7b5?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D25716737-46ad970e-dc9e-4246-bac2-769c6083e7b5%26entityType%3Dcollection%26workspaceId%3Da8d63f9f-cfc7-4810-90c5-9e0c60030d3e#?env%5BAdyen%20APIs%5D=W3sia2V5IjoiWC1BUEktS2V5IiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoic2VjcmV0In0seyJrZXkiOiJZT1VSX01FUkNIQU5UX0FDQ09VTlQiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0In0seyJrZXkiOiJZT1VSX0NPTVBBTllfQUNDT1VOVCIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQifSx7ImtleSI6IllPVVJfQkFMQU5DRV9QTEFURk9STSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQifV0=)

### Going live

To access the live endpoints, you need an API key from your live Customer Area.

The live endpoint URLs contain a prefix which is unique to your company account, for example:

```
https://{PREFIX}-checkout-live.adyenpayments.com/checkout/v71/payments
```

Get your `{PREFIX}` from your live Customer Area under **Developers** > **API URLs** > **Prefix**.

When preparing to do live transactions with Checkout API, follow the [go-live checklist](https://docs.adyen.com/online-payments/go-live-checklist) to make sure you've got all the required configuration in place.

### Release notes

Have a look at the [release notes](https://docs.adyen.com/online-payments/release-notes?integration_type=api&version=71) to find out what changed in this version!, Configure and manage your Adyen company and merchant accounts, stores, and payment terminals.

### Authentication

Each request to the Management API must be signed with an API key. [Generate your API key](https://docs.adyen.com/development-resources/api-credentials#generate-api-key) in the Customer Area and then set this key to the `X-API-Key` header value.

To access the live endpoints, you need to generate a new API key in your live Customer Area.

### Versioning

Management API handles versioning as part of the endpoint URL. For example, to send a request to this version of the `/companies/{companyId}/webhooks` endpoint, use:

```text
https://management-test.adyen.com/v3/companies/{companyId}/webhooks
```

### Going live

To access the live endpoints, you need an API key from your live Customer Area. Use this API key to make requests to:

```text
https://management-live.adyen.com/v3
```

### Release notes

Have a look at the [release notes](https://docs.adyen.com/release-notes/management-api) to find out what changed in this version!

## Install the Package

Run the following command to install the package and automatically add the dependency to your composer.json file:

```bash
composer require "apimatic-adyen/adyen-apimatic-sdk:1.0.1"
```

Or add it to the composer.json file manually as given below:

```json
"require": {
    "apimatic-adyen/adyen-apimatic-sdk": "1.0.1"
}
```

You can also view the package at:
https://packagist.org/packages/apimatic-adyen/adyen-apimatic-sdk#1.0.1

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| timeout | `int` | Timeout for API calls in seconds.<br>*Default*: `30` |
| enableRetries | `bool` | Whether to enable retries and backoff feature.<br>*Default*: `false` |
| numberOfRetries | `int` | The number of retries to make.<br>*Default*: `0` |
| retryInterval | `float` | The retry time interval between the endpoint calls.<br>*Default*: `1` |
| backOffFactor | `float` | Exponential backoff factor to increase interval between retries.<br>*Default*: `2` |
| maximumRetryWaitTime | `int` | The maximum wait time in seconds for overall retrying requests.<br>*Default*: `0` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` |
| httpStatusCodesToRetry | `array` | Http status codes to retry against.<br>*Default*: `408, 413, 429, 500, 502, 503, 504, 521, 522, 524` |
| httpMethodsToRetry | `array` | Http methods to retry against.<br>*Default*: `'GET', 'PUT'` |
| loggingConfiguration | [`LoggingConfigurationBuilder`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/logging-configuration-builder.md) | Represents the logging configurations for API calls |
| proxyConfiguration | [`ProxyConfigurationBuilder`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/proxy-configuration-builder.md) | Represents the proxy configurations for API calls |
| apiKeyAuthCredentials | [`ApiKeyAuthCredentials`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| basicAuthCredentials | [`BasicAuthCredentials`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/auth/basic-authentication.md) | The Credentials Setter for Basic Authentication |

The API client can be initialized as follows:

```php
use AdyenApIsLib\Logging\LoggingConfigurationBuilder;
use AdyenApIsLib\Logging\RequestLoggingConfigurationBuilder;
use AdyenApIsLib\Logging\ResponseLoggingConfigurationBuilder;
use Psr\Log\LogLevel;
use AdyenApIsLib\Environment;
use AdyenApIsLib\Authentication\ApiKeyAuthCredentialsBuilder;
use AdyenApIsLib\Authentication\BasicAuthCredentialsBuilder;
use AdyenApIsLib\AdyenApIsClientBuilder;

$client = AdyenApIsClientBuilder::init()
    ->apiKeyAuthCredentials(
        ApiKeyAuthCredentialsBuilder::init(
            'X-API-Key'
        )
    )
    ->basicAuthCredentials(
        BasicAuthCredentialsBuilder::init(
            'Username',
            'Password'
        )
    )
    ->environment(Environment::PRODUCTION)
    ->loggingConfiguration(
        LoggingConfigurationBuilder::init()
            ->level(LogLevel::INFO)
            ->requestConfiguration(RequestLoggingConfigurationBuilder::init()->body(true))
            ->responseConfiguration(ResponseLoggingConfigurationBuilder::init()->headers(true))
    )
    ->build();
```

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`ApiKeyAuth (Custom Header Signature)`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/auth/custom-header-signature.md)
* [`BasicAuth (Basic Authentication)`](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/auth/basic-authentication.md)

## List of APIs

* [Paymentlinks](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/paymentlinks.md)
* [Account-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/account-companylevel.md)
* [Account-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/account-merchantlevel.md)
* [Account-Storelevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/account-storelevel.md)
* [Payoutsettings-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/payoutsettings-merchantlevel.md)
* [Users-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/users-companylevel.md)
* [Users-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/users-merchantlevel.md)
* [My AP Icredential](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/my-ap-icredential.md)
* [AP Icredentials-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/ap-icredentials-companylevel.md)
* [AP Icredentials-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/ap-icredentials-merchantlevel.md)
* [AP Ikey-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/ap-ikey-companylevel.md)
* [AP Ikey-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/ap-ikey-merchantlevel.md)
* [Clientkey-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/clientkey-companylevel.md)
* [Clientkey-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/clientkey-merchantlevel.md)
* [Allowedorigins-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/allowedorigins-companylevel.md)
* [Allowedorigins-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/allowedorigins-merchantlevel.md)
* [Webhooks-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/webhooks-companylevel.md)
* [Webhooks-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/webhooks-merchantlevel.md)
* [Paymentmethods-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/paymentmethods-merchantlevel.md)
* [Terminals-Terminallevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminals-terminallevel.md)
* [Terminalactions-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalactions-companylevel.md)
* [Terminalactions-Terminallevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalactions-terminallevel.md)
* [Terminalorders-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalorders-companylevel.md)
* [Terminalorders-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalorders-merchantlevel.md)
* [Terminalsettings-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalsettings-companylevel.md)
* [Terminalsettings-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalsettings-merchantlevel.md)
* [Terminalsettings-Storelevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalsettings-storelevel.md)
* [Terminalsettings-Terminallevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/terminalsettings-terminallevel.md)
* [Androidfiles-Companylevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/androidfiles-companylevel.md)
* [Splitconfiguration-Merchantlevel](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/splitconfiguration-merchantlevel.md)
* [Payments](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/payments.md)
* [Donations](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/donations.md)
* [Modifications](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/modifications.md)
* [Recurring](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/recurring.md)
* [Orders](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/orders.md)
* [Utility](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/controllers/utility.md)

## SDK Infrastructure

### Configuration

* [ProxyConfigurationBuilder](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/proxy-configuration-builder.md)
* [LoggingConfigurationBuilder](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/logging-configuration-builder.md)
* [RequestLoggingConfigurationBuilder](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/request-logging-configuration-builder.md)
* [ResponseLoggingConfigurationBuilder](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/response-logging-configuration-builder.md)

### HTTP

* [HttpRequest](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/adyen-apimatic-php-sdk/tree/1.0.1/doc/api-response.md)

