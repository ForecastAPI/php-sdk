# ForecastAPI\Sdk\DefaultApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deprecatedV1()**](DefaultApi.md#deprecatedV1) | **GET** /v1/{any} | Deprecated v1 endpoints |


## `deprecatedV1()`

```php
deprecatedV1($any)
```

Deprecated v1 endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ForecastAPI\Sdk\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$any = 'any_example'; // string

try {
    $apiInstance->deprecatedV1($any);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->deprecatedV1: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **any** | **string**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
