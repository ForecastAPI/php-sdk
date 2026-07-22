# ForecastAPI\Sdk\GroupedForecastingApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createGroupedForecast()**](GroupedForecastingApi.md#createGroupedForecast) | **POST** /v2/forecast/grouped | Submit a grouped (hierarchical) forecast with reconciliation |
| [**getGroupedForecast()**](GroupedForecastingApi.md#getGroupedForecast) | **GET** /v2/forecast/grouped/{grouped_forecast_id} | Poll a grouped forecast for status and results |


## `createGroupedForecast()`

```php
createGroupedForecast($grouped_forecast_request): \ForecastAPI\Sdk\Model\GroupedForecastAccepted
```

Submit a grouped (hierarchical) forecast with reconciliation

Forecast a set of related series that roll up to a total — MRR by plan and region, demand by warehouse, revenue by category — and get back one coherent result: every parent equals the sum of its children, in every period, at every level.  You send only the **leaves** of the hierarchy (every combination of the declared dimensions, each with its own history). The API derives every aggregate level and the grand total by summing the leaf histories, forecasts the nodes, reconciles them to coherence, and stores each node as its own entity with independently tracked accuracy.  Processing is **asynchronous**: submission returns `202` with an id to poll via `GET /v2/forecast/grouped/{grouped_forecast_id}`. The run executes in the background as one all-or-nothing job — a hierarchy is one coherent answer, so there is no partial success. If any node cannot be forecast, the run fails with the reason rather than returning numbers that don't add up.  If you just want independent forecasts per slice — no coherent roll-up — the batch endpoint with per-series identifiers or `tenant_context` is simpler and tolerates per-series failure.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\GroupedForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$grouped_forecast_request = {"identifier":"mrr","hierarchy":["region","plan"],"reconciliation":"bottom_up","frequency":"M","periods":6,"data_type":"revenue","series":[{"segment":{"region":"eu","plan":"pro"},"data":[{"date":"2024-01-01","value":42000},{"date":"2024-02-01","value":43800}]},{"segment":{"region":"eu","plan":"free"},"data":[{"date":"2024-01-01","value":3100},{"date":"2024-02-01","value":3300}]},{"segment":{"region":"us","plan":"pro"},"data":[{"date":"2024-01-01","value":61000},{"date":"2024-02-01","value":62500}]}]}; // \ForecastAPI\Sdk\Model\GroupedForecastRequest

try {
    $result = $apiInstance->createGroupedForecast($grouped_forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupedForecastingApi->createGroupedForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **grouped_forecast_request** | [**\ForecastAPI\Sdk\Model\GroupedForecastRequest**](../Model/GroupedForecastRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\GroupedForecastAccepted**](../Model/GroupedForecastAccepted.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupedForecast()`

```php
getGroupedForecast($grouped_forecast_id): \ForecastAPI\Sdk\Model\GroupedForecastStatusResponse
```

Poll a grouped forecast for status and results

Returns the run's status. Once `completed`, `results` carries a node map keyed by segment (`total`, `region=eu`, `plan=pro|region=eu`, …) — every node with its own forecast rows, its place in the tree, and the reconciliation details. If the run `failed`, `error` carries the reason and `results` stays null.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\GroupedForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$grouped_forecast_id = k3n9x2m4p8q1w5r7; // string | The id returned by POST /v2/forecast/grouped

try {
    $result = $apiInstance->getGroupedForecast($grouped_forecast_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupedForecastingApi->getGroupedForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **grouped_forecast_id** | **string**| The id returned by POST /v2/forecast/grouped | |

### Return type

[**\ForecastAPI\Sdk\Model\GroupedForecastStatusResponse**](../Model/GroupedForecastStatusResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
