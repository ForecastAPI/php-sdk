# ForecastAPI\ForecastSDK\ForecastingApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v2ForecastPost()**](ForecastingApi.md#v2ForecastPost) | **POST** /v2/forecast | Generate forecast for time series data |


## `v2ForecastPost()`

```php
v2ForecastPost($forecast_request): \ForecastAPI\ForecastSDK\Model\ForecastResponse
```

Generate forecast for time series data

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\ForecastSDK\Api\ForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forecast_request = new \ForecastAPI\ForecastSDK\Model\ForecastRequest(); // \ForecastAPI\ForecastSDK\Model\ForecastRequest

try {
    $result = $apiInstance->v2ForecastPost($forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ForecastingApi->v2ForecastPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forecast_request** | [**\ForecastAPI\ForecastSDK\Model\ForecastRequest**](../Model/ForecastRequest.md)|  | |

### Return type

[**\ForecastAPI\ForecastSDK\Model\ForecastResponse**](../Model/ForecastResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
