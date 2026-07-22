# ForecastAPI\Sdk\AnomalyDetectionApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**detectAnomalies()**](AnomalyDetectionApi.md#detectAnomalies) | **POST** /v2/detect-anomalies | Detect anomalies in time series data |


## `detectAnomalies()`

```php
detectAnomalies($anomaly_detection_request): \ForecastAPI\Sdk\Model\AnomalyDetectionResponse
```

Detect anomalies in time series data

Detects anomalies using statistical methods — z-score, IQR or seasonal — and automatically selects the best method for the data's characteristics unless one is named in `anomaly_settings.method`. Returns each anomalous point with its expected range, severity and type, plus an analysis of how the method was chosen.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\AnomalyDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$anomaly_detection_request = new \ForecastAPI\Sdk\Model\AnomalyDetectionRequest(); // \ForecastAPI\Sdk\Model\AnomalyDetectionRequest

try {
    $result = $apiInstance->detectAnomalies($anomaly_detection_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnomalyDetectionApi->detectAnomalies: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **anomaly_detection_request** | [**\ForecastAPI\Sdk\Model\AnomalyDetectionRequest**](../Model/AnomalyDetectionRequest.md)|  | |

### Return type

[**\ForecastAPI\Sdk\Model\AnomalyDetectionResponse**](../Model/AnomalyDetectionResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
