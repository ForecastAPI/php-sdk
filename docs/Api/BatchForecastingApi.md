# ForecastAPI\Sdk\BatchForecastingApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBatchForecast()**](BatchForecastingApi.md#createBatchForecast) | **POST** /v2/batch/forecast | Submit a batch of series for forecasting |
| [**getBatchForecast()**](BatchForecastingApi.md#getBatchForecast) | **GET** /v2/batch/forecast/{batch_id} | Poll a batch forecast for status and results |
| [**presignBatchForecast()**](BatchForecastingApi.md#presignBatchForecast) | **POST** /v2/batch/forecast/presign | Get a presigned URL for a file-based batch upload |


## `createBatchForecast()`

```php
createBatchForecast($batch_forecast_request): \ForecastAPI\Sdk\Model\BatchForecastAccepted
```

Submit a batch of series for forecasting

Forecast up to 100,000 independent series in one call (10 on the free tier), at a discount per forecast. Each series is processed independently — one failing series does not fail the others. Submission returns `202` with a `batch_id` to poll via `GET /v2/batch/forecast/{batch_id}`.  Request-level `periods`, `frequency`, `data_type`, `confidence` and the four planning parameters (`quantiles`, `value_bounds`, `adjustments`, `accumulate`) act as defaults every series inherits; any series may override any of them. `model` is request-level only.  For payloads too large to send inline, get a presigned upload URL from `POST /v2/batch/forecast/presign` and submit `file_key` instead of `series`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\BatchForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_forecast_request = {"series":[{"identifier":"SKU-001","data":[{"date":"2024-01-01","value":100},{"date":"2024-02-01","value":150}],"data_type":"sales","periods":3},{"identifier":"CHURN-RATE","data":[{"date":"2024-01-01","value":0.041},{"date":"2024-02-01","value":0.038}],"periods":3,"value_bounds":{"min":0,"max":1}}],"frequency":"M","confidence":0.8,"quantiles":[0.1,0.5,0.9]}; // \ForecastAPI\Sdk\Model\BatchForecastRequest

try {
    $result = $apiInstance->createBatchForecast($batch_forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchForecastingApi->createBatchForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_forecast_request** | [**\ForecastAPI\Sdk\Model\BatchForecastRequest**](../Model/BatchForecastRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\BatchForecastAccepted**](../Model/BatchForecastAccepted.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBatchForecast()`

```php
getBatchForecast($batch_id): \ForecastAPI\Sdk\Model\BatchForecastStatusResponse
```

Poll a batch forecast for status and results

Returns the batch's status, a summary once it finalises, and each series' results under `results.data` — keyed by **entity id** rather than by your identifier, because one batch may contain the same identifier under several `tenant_context` values. Match series via the `identifier` and `tenant_context` echoed inside each result object.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\BatchForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string | The id returned by POST /v2/batch/forecast

try {
    $result = $apiInstance->getBatchForecast($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchForecastingApi->getBatchForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**| The id returned by POST /v2/batch/forecast | |

### Return type

[**\ForecastAPI\Sdk\Model\BatchForecastStatusResponse**](../Model/BatchForecastStatusResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `presignBatchForecast()`

```php
presignBatchForecast(): \ForecastAPI\Sdk\Model\BatchPresignResponse
```

Get a presigned URL for a file-based batch upload

Returns a presigned URL for uploading a JSON file containing the batch request body — an object with a `series` array, the same shape as the inline `/v2/batch/forecast` request. HTTP PUT the file to `upload_url` (including any returned `headers`), then submit the batch by POSTing the returned `file_key` to `/v2/batch/forecast`. The URL is valid for 30 minutes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\BatchForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->presignBatchForecast();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchForecastingApi->presignBatchForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ForecastAPI\Sdk\Model\BatchPresignResponse**](../Model/BatchPresignResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
