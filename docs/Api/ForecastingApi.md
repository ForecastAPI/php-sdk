# ForecastAPI\Sdk\ForecastingApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createForecast()**](ForecastingApi.md#createForecast) | **POST** /v2/forecast | Generate forecast for time series data |


## `createForecast()`

```php
createForecast($forecast_request): \ForecastAPI\Sdk\Model\ForecastResponse
```

Generate forecast for time series data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\ForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forecast_request = new \ForecastAPI\Sdk\Model\ForecastRequest(); // \ForecastAPI\Sdk\Model\ForecastRequest

try {
    $result = $apiInstance->createForecast($forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ForecastingApi->createForecast: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forecast_request** | [**\ForecastAPI\Sdk\Model\ForecastRequest**](../Model/ForecastRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\ForecastResponse**](../Model/ForecastResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
