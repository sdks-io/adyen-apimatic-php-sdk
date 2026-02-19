
# Custom Header Signature



Documentation for accessing and setting credentials for ApiKeyAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| X-API-Key | `string` | - | `xApiKey` | `getXApiKey()` |



**Note:** Auth credentials can be set using `ApiKeyAuthCredentialsBuilder::init()` in `apiKeyAuthCredentials` method in the client builder and accessed through `getApiKeyAuthCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```php
use AdyenApIsLib\Authentication\ApiKeyAuthCredentialsBuilder;
use AdyenApIsLib\AdyenApIsClientBuilder;

$client = AdyenApIsClientBuilder::init()
    ->apiKeyAuthCredentials(
        ApiKeyAuthCredentialsBuilder::init(
            'X-API-Key'
        )
    )
    ->build();
```


