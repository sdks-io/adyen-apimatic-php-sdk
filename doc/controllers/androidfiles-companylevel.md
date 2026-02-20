# Androidfiles-Companylevel

```php
$androidfilesCompanylevelApi = $client->getAndroidfilesCompanylevelApi();
```

## Class Name

`AndroidfilesCompanylevelApi`

## Methods

* [List Android Apps](../../doc/controllers/androidfiles-companylevel.md#list-android-apps)
* [Create Android App](../../doc/controllers/androidfiles-companylevel.md#create-android-app)
* [Get Android App](../../doc/controllers/androidfiles-companylevel.md#get-android-app)
* [Update Android App](../../doc/controllers/androidfiles-companylevel.md#update-android-app)
* [List Android Certificates](../../doc/controllers/androidfiles-companylevel.md#list-android-certificates)
* [Upload Android Certificate](../../doc/controllers/androidfiles-companylevel.md#upload-android-certificate)


# List Android Apps

Returns a list of the Android apps that are available for the company identified in the path.
These apps have been uploaded to Adyen and can be installed or uninstalled on Android payment terminals through [terminal actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Android files read
* Management API—Android files read and write
* Management API—Terminal actions read
* Management API—Terminal actions read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function listAndroidApps(
    string $companyId,
    ?int $pageNumber = null,
    ?int $pageSize = null,
    ?string $packageName = null,
    ?int $versionCode = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 20 items on a page. |
| `packageName` | `?string` | Query, Optional | The package name that uniquely identifies the Android app. |
| `versionCode` | `?int` | Query, Optional | The version number of the app. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AndroidAppsResponse`](../../doc/models/android-apps-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->listAndroidApps($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AndroidAppsResponse:';
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
      "id": "ANDA422LZ223223K5F694GCCF732K8",
      "packageName": "com.your_company.posapp",
      "versionCode": 7700203,
      "description": "POS2",
      "label": "POS system",
      "versionName": "7.7",
      "status": "ready"
    },
    {
      "id": "ANDA422LZ223223K5F694FWCF738PL",
      "packageName": "com.your_company.posapp",
      "versionCode": 7602003,
      "description": "POS1",
      "label": "POS system",
      "versionName": "7.6",
      "status": "ready"
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


# Create Android App

Uploads an Android APK file to Adyen.
The maximum APK file size is 200 MB.
To make this request, your API credential must have the following [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Android files read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

> By choosing to upload, install, or run any third-party applications on an Adyen payment terminal, you accept full responsibility and liability for any consequences of uploading, installing, or running any such applications.

```php
function createAndroidApp(string $companyId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UploadAndroidAppResponse`](../../doc/models/upload-android-app-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->createAndroidApp($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UploadAndroidAppResponse:';
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


# Get Android App

Returns the details of the Android app identified in the path.
These apps have been uploaded to Adyen and can be installed or uninstalled on Android payment terminals through [terminal actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Android files read
* Management API—Android files read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function getAndroidApp(string $companyId, string $id): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `id` | `string` | Template, Required | The unique identifier of the app. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AndroidApp`](../../doc/models/android-app.md).

## Example Usage

```php
$companyId = 'companyId0';

$id = 'id0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->getAndroidApp(
    $companyId,
    $id
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AndroidApp:';
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


# Update Android App

Reuploads the Android app identified in the path.
To make this request, your API credential must have this [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Android files read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

> By choosing to upload, install, or run any third-party applications on an Adyen payment terminal, you accept full responsibility and liability for any consequences of uploading, installing, or running any such applications.

```php
function updateAndroidApp(string $companyId, string $id): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `id` | `string` | Template, Required | The unique identifier of the app. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ReprocessAndroidAppResponse`](../../doc/models/reprocess-android-app-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$id = 'id0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->updateAndroidApp(
    $companyId,
    $id
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ReprocessAndroidAppResponse:';
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


# List Android Certificates

Returns a list of the Android certificates that are available for the company identified in the path.
Typically, these certificates enable running apps on Android payment terminals. The certificates in the list have been uploaded to Adyen and can be installed or uninstalled on Android terminals through [terminal actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).

To make this request, your API credential must have one of the following [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

* Management API—Android files read
* Management API—Android files read and write
* Management API—Terminal actions read
* Management API—Terminal actions read and write

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function listAndroidCertificates(
    string $companyId,
    ?int $pageNumber = null,
    ?int $pageSize = null,
    ?string $certificateName = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |
| `pageNumber` | `?int` | Query, Optional | The number of the page to fetch. |
| `pageSize` | `?int` | Query, Optional | The number of items to have on a page, maximum 100. The default is 20 items on a page. |
| `certificateName` | `?string` | Query, Optional | The name of the certificate. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AndroidCertificatesResponse`](../../doc/models/android-certificates-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->listAndroidCertificates($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AndroidCertificatesResponse:';
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
      "id": "ANDC422LZ223223K5F78NVN9SL4VPH",
      "name": "mycert",
      "extension": ".crt",
      "description": "",
      "status": "ready",
      "notBefore": "2008-04-20T00:00:00+02:00",
      "notAfter": "2038-04-12T00:00:00+02:00"
    },
    {
      "id": "ANDC533MA33433L689OWO0TM5WQI",
      "name": "mynewcert",
      "extension": ".pem",
      "description": "",
      "status": "ready",
      "notBefore": "2008-04-20T00:00:00+02:00",
      "notAfter": "2048-04-12T00:00:00+02:00"
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


# Upload Android Certificate

Uploads an Android Certificate file to Adyen.

In the live environment, requests to this endpoint are subject to [rate limits](https://docs.adyen.com/point-of-sale/automating-terminal-management#rate-limits-in-the-live-environment).

```php
function uploadAndroidCertificate(string $companyId): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `companyId` | `string` | Template, Required | The unique identifier of the company account. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UploadAndroidCertificateResponse`](../../doc/models/upload-android-certificate-response.md).

## Example Usage

```php
$companyId = 'companyId0';

$androidFilesCompanyLevelApi = $client->getAndroidFilesCompanyLevelApi();
$apiResponse = $androidFilesCompanyLevelApi->uploadAndroidCertificate($companyId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UploadAndroidCertificateResponse:';
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

