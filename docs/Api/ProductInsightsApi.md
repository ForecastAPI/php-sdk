# ForecastAPI\Sdk\ProductInsightsApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBatchProductInsights()**](ProductInsightsApi.md#createBatchProductInsights) | **POST** /v2/batch/product-insights | Submit a batch of products for insights analysis |
| [**createProductInsights()**](ProductInsightsApi.md#createProductInsights) | **POST** /v2/product-insights | Analyze product performance for anomalies, trends and business insights |
| [**getProductInsightsBatch()**](ProductInsightsApi.md#getProductInsightsBatch) | **GET** /v2/batch/product-insights/{batch_id} | Poll a product insights batch for status and results |


## `createBatchProductInsights()`

```php
createBatchProductInsights($product_insights_batch_request): \ForecastAPI\Sdk\Model\ProductInsightsBatchStatusResponse
```

Submit a batch of products for insights analysis

Analyze up to 1,000 products in one asynchronous batch; each entry is the same shape as a single `/v2/product-insights` request. Returns `202` with the batch resource to poll via `GET /v2/batch/product-insights/{batch_id}`. The optional `batch` and `parts` fields let a large batch be submitted in chunks that share one batch id. Validation is per series: if any entry fails, the whole submission is rejected with the failing entries listed by index.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\ProductInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_insights_batch_request = new \ForecastAPI\Sdk\Model\ProductInsightsBatchRequest(); // \ForecastAPI\Sdk\Model\ProductInsightsBatchRequest

try {
    $result = $apiInstance->createBatchProductInsights($product_insights_batch_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductInsightsApi->createBatchProductInsights: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_insights_batch_request** | [**\ForecastAPI\Sdk\Model\ProductInsightsBatchRequest**](../Model/ProductInsightsBatchRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\ProductInsightsBatchStatusResponse**](../Model/ProductInsightsBatchStatusResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createProductInsights()`

```php
createProductInsights($product_insights_request): \ForecastAPI\Sdk\Model\ProductInsightsResponse
```

Analyze product performance for anomalies, trends and business insights

Analyzes a product's sales, purchase and cost-history data and returns classified insights — margin compression, sales anomalies, cost changes, lead-time reliability and more — each with severity, the metrics behind it and a recommendation. At least one of `sales`, `purchases` or `cost_history` must be provided. Analyses are stored per product, so repeat calls also return a `comparison` against the previous analysis with a new/changed/resolved breakdown.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\ProductInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_insights_request = new \ForecastAPI\Sdk\Model\ProductInsightsRequest(); // \ForecastAPI\Sdk\Model\ProductInsightsRequest

try {
    $result = $apiInstance->createProductInsights($product_insights_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductInsightsApi->createProductInsights: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_insights_request** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequest**](../Model/ProductInsightsRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\ProductInsightsResponse**](../Model/ProductInsightsResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductInsightsBatch()`

```php
getProductInsightsBatch($batch_id): \ForecastAPI\Sdk\Model\ProductInsightsBatchStatusResponse
```

Poll a product insights batch for status and results

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\ProductInsightsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_id = 'batch_id_example'; // string | The batch identifier returned on submission

try {
    $result = $apiInstance->getProductInsightsBatch($batch_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductInsightsApi->getProductInsightsBatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_id** | **string**| The batch identifier returned on submission | |

### Return type

[**\ForecastAPI\Sdk\Model\ProductInsightsBatchStatusResponse**](../Model/ProductInsightsBatchStatusResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
