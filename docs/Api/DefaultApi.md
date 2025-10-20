# ForecastAPI\ForecastSDK\DefaultApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AnyGet()**](DefaultApi.md#v1AnyGet) | **GET** /v1/{any} | Deprecated v1 endpoints |


## `v1AnyGet()`

```php
v1AnyGet($any)
```

Deprecated v1 endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ForecastAPI\ForecastSDK\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$any = 'any_example'; // string

try {
    $apiInstance->v1AnyGet($any);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->v1AnyGet: ', $e->getMessage(), PHP_EOL;
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
