# ForecastAPI\ForecastSDK\TrafficForecastingApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v2TrafficForecastingPost()**](TrafficForecastingApi.md#v2TrafficForecastingPost) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations |


## `v2TrafficForecastingPost()`

```php
v2TrafficForecastingPost($traffic_forecasting_request): \ForecastAPI\ForecastSDK\Model\TrafficForecastingResponse
```

Generate traffic forecasting with infrastructure scaling recommendations

Generate comprehensive traffic forecasts with infrastructure scaling recommendations, capacity analysis, cost optimization, and traffic anomaly alerts. This endpoint is designed for web applications, APIs, and infrastructure teams to predict traffic patterns and optimize resource allocation.  **Key Features:** - Intelligent traffic pattern forecasting with multiple algorithms - Infrastructure scaling recommendations (scale up/down/maintain) - Real-time capacity utilization analysis - Traffic spike and anomaly detection alerts - Cost optimization recommendations with potential savings - Auto-scaling benefit analysis - Support for various time frequencies (minute, hourly, daily, etc.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\ForecastSDK\Api\TrafficForecastingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$traffic_forecasting_request = {"identifier":"api-endpoint-users","frequency":"H","start_date":"2024-01-01","periods":24,"enable_intelligent_aggregation":true,"data":[{"date":"2023-12-01 00:00:00","value":1200},{"date":"2023-12-01 01:00:00","value":800},{"date":"2023-12-01 02:00:00","value":600},{"date":"2023-12-01 03:00:00","value":500},{"date":"2023-12-01 04:00:00","value":450}],"traffic_settings":{"current_capacity":2000,"baseline_traffic":1000,"scaling_buffer":0.2,"scale_up_threshold":0.8,"scale_down_threshold":0.3,"alert_threshold":1.5,"anomaly_threshold":3.0,"cost_per_unit":0.01,"fixed_cost_per_capacity":0.1,"base_scaling_time":5,"enable_auto_scaling":false}}; // \ForecastAPI\ForecastSDK\Model\TrafficForecastingRequest

try {
    $result = $apiInstance->v2TrafficForecastingPost($traffic_forecasting_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrafficForecastingApi->v2TrafficForecastingPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **traffic_forecasting_request** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingRequest**](../Model/TrafficForecastingRequest.md)|  | |

### Return type

[**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponse**](../Model/TrafficForecastingResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
