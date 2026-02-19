
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| timeout | `int` | Timeout for API calls in seconds.<br>*Default*: `30` |
| enableRetries | `bool` | Whether to enable retries and backoff feature.<br>*Default*: `false` |
| numberOfRetries | `int` | The number of retries to make.<br>*Default*: `0` |
| retryInterval | `float` | The retry time interval between the endpoint calls.<br>*Default*: `1` |
| backOffFactor | `float` | Exponential backoff factor to increase interval between retries.<br>*Default*: `2` |
| maximumRetryWaitTime | `int` | The maximum wait time in seconds for overall retrying requests.<br>*Default*: `0` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` |
| httpStatusCodesToRetry | `array` | Http status codes to retry against.<br>*Default*: `408, 413, 429, 500, 502, 503, 504, 521, 522, 524` |
| httpMethodsToRetry | `array` | Http methods to retry against.<br>*Default*: `'GET', 'PUT'` |
| loggingConfiguration | [`LoggingConfigurationBuilder`](../doc/logging-configuration-builder.md) | Represents the logging configurations for API calls |
| proxyConfiguration | [`ProxyConfigurationBuilder`](../doc/proxy-configuration-builder.md) | Represents the proxy configurations for API calls |
| apiKeyAuthCredentials | [`ApiKeyAuthCredentials`](auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| basicAuthCredentials | [`BasicAuthCredentials`](auth/basic-authentication.md) | The Credentials Setter for Basic Authentication |

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

## Adyen APIs Client

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

## Apis

| Name | Description |
|  --- | --- |
| getPaymentsApi() | Gets PaymentsApi |
| getDonationsApi() | Gets DonationsApi |
| getPaymentLinksApi() | Gets PaymentLinksApi |
| getModificationsApi() | Gets ModificationsApi |
| getRecurringApi() | Gets RecurringApi |
| getOrdersApi() | Gets OrdersApi |
| getUtilityApi() | Gets UtilityApi |
| getAccountCompanyLevelApi() | Gets AccountCompanyLevelApi |
| getAccountMerchantLevelApi() | Gets AccountMerchantLevelApi |
| getAccountStoreLevelApi() | Gets AccountStoreLevelApi |
| getPayoutSettingsMerchantLevelApi() | Gets PayoutSettingsMerchantLevelApi |
| getUsersCompanyLevelApi() | Gets UsersCompanyLevelApi |
| getUsersMerchantLevelApi() | Gets UsersMerchantLevelApi |
| getMyApiCredentialApi() | Gets MyApiCredentialApi |
| getApiCredentialsCompanyLevelApi() | Gets ApiCredentialsCompanyLevelApi |
| getApiCredentialsMerchantLevelApi() | Gets ApiCredentialsMerchantLevelApi |
| getApiKeyCompanyLevelApi() | Gets ApiKeyCompanyLevelApi |
| getApiKeyMerchantLevelApi() | Gets ApiKeyMerchantLevelApi |
| getClientKeyCompanyLevelApi() | Gets ClientKeyCompanyLevelApi |
| getClientKeyMerchantLevelApi() | Gets ClientKeyMerchantLevelApi |
| getAllowedOriginsCompanyLevelApi() | Gets AllowedOriginsCompanyLevelApi |
| getAllowedOriginsMerchantLevelApi() | Gets AllowedOriginsMerchantLevelApi |
| getWebhooksCompanyLevelApi() | Gets WebhooksCompanyLevelApi |
| getWebhooksMerchantLevelApi() | Gets WebhooksMerchantLevelApi |
| getPaymentMethodsMerchantLevelApi() | Gets PaymentMethodsMerchantLevelApi |
| getTerminalsTerminalLevelApi() | Gets TerminalsTerminalLevelApi |
| getTerminalActionsCompanyLevelApi() | Gets TerminalActionsCompanyLevelApi |
| getTerminalActionsTerminalLevelApi() | Gets TerminalActionsTerminalLevelApi |
| getTerminalOrdersCompanyLevelApi() | Gets TerminalOrdersCompanyLevelApi |
| getTerminalOrdersMerchantLevelApi() | Gets TerminalOrdersMerchantLevelApi |
| getTerminalSettingsCompanyLevelApi() | Gets TerminalSettingsCompanyLevelApi |
| getTerminalSettingsMerchantLevelApi() | Gets TerminalSettingsMerchantLevelApi |
| getTerminalSettingsStoreLevelApi() | Gets TerminalSettingsStoreLevelApi |
| getTerminalSettingsTerminalLevelApi() | Gets TerminalSettingsTerminalLevelApi |
| getAndroidFilesCompanyLevelApi() | Gets AndroidFilesCompanyLevelApi |
| getSplitConfigurationMerchantLevelApi() | Gets SplitConfigurationMerchantLevelApi |

