# ForecastAPI\ForecastSDK\InventoryPlanningApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v2InventoryPlanningPost()**](InventoryPlanningApi.md#v2InventoryPlanningPost) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations |


## `v2InventoryPlanningPost()`

```php
v2InventoryPlanningPost($inventory_planning_request): \ForecastAPI\ForecastSDK\Model\InventoryPlanningResponse
```

Generate comprehensive inventory planning recommendations

Generate inventory forecasts with supplier recommendations, reorder points, safety stock calculations, and comprehensive stock analysis. This endpoint combines time series forecasting with inventory optimization to provide actionable recommendations for stock management and procurement.  **Key Features:** - Automatic forecasting method selection based on demand patterns - Multi-supplier cost and lead time optimization - Safety stock calculation with configurable service levels - Reorder point recommendations with minimum order quantity considerations - Stock analysis including stockout risk and days of coverage - Real-time supplier performance evaluation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\ForecastSDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\ForecastSDK\Api\InventoryPlanningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_planning_request = {"identifier":"SKU-12345","frequency":"M","start_date":"2024-01-01","periods":6,"enable_intelligent_aggregation":true,"data":[{"date":"2023-01-01","value":100},{"date":"2023-02-01","value":120},{"date":"2023-03-01","value":95},{"date":"2023-04-01","value":130},{"date":"2023-05-01","value":110}],"inventory_settings":{"current_stock":250,"minimum_stock":50,"service_level":0.95,"suppliers":[{"identifier":"supplier-a","lead_time_days":14,"minimum_order_quantity":100,"cost_per_unit":12.5,"reliability_score":0.98}]}}; // \ForecastAPI\ForecastSDK\Model\InventoryPlanningRequest

try {
    $result = $apiInstance->v2InventoryPlanningPost($inventory_planning_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryPlanningApi->v2InventoryPlanningPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_planning_request** | [**\ForecastAPI\ForecastSDK\Model\InventoryPlanningRequest**](../Model/InventoryPlanningRequest.md)|  | |

### Return type

[**\ForecastAPI\ForecastSDK\Model\InventoryPlanningResponse**](../Model/InventoryPlanningResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
