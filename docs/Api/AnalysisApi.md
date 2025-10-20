# ForecastAPI\ForecastSDK\AnalysisApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v2AnalyzePost()**](AnalysisApi.md#v2AnalyzePost) | **POST** /v2/analyze | Analyze time series data without generating forecast |


## `v2AnalyzePost()`

```php
v2AnalyzePost($forecast_request): \ForecastAPI\ForecastSDK\Model\AnalysisResponse
```

Analyze time series data without generating forecast

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\ForecastSDK\Api\AnalysisApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forecast_request = new \ForecastAPI\ForecastSDK\Model\ForecastRequest(); // \ForecastAPI\ForecastSDK\Model\ForecastRequest

try {
    $result = $apiInstance->v2AnalyzePost($forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalysisApi->v2AnalyzePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forecast_request** | [**\ForecastAPI\ForecastSDK\Model\ForecastRequest**](../Model/ForecastRequest.md)|  | |

### Return type

[**\ForecastAPI\ForecastSDK\Model\AnalysisResponse**](../Model/AnalysisResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
