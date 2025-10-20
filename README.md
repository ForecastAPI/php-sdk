# forecastapi/php-sdk

Time series forecasting service with multiple algorithms and automatic method selection


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/forecastapi/php-sdk.git"
    }
  ],
  "require": {
    "forecastapi/php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/forecastapi/php-sdk/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://forecastapi.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalysisApi* | [**v2AnalyzePost**](docs/Api/AnalysisApi.md#v2analyzepost) | **POST** /v2/analyze | Analyze time series data without generating forecast
*DefaultApi* | [**v1AnyGet**](docs/Api/DefaultApi.md#v1anyget) | **GET** /v1/{any} | Deprecated v1 endpoints
*ForecastingApi* | [**v2ForecastPost**](docs/Api/ForecastingApi.md#v2forecastpost) | **POST** /v2/forecast | Generate forecast for time series data
*HealthApi* | [**v2Get**](docs/Api/HealthApi.md#v2get) | **GET** /v2 | API root endpoint
*HealthApi* | [**v2HealthGet**](docs/Api/HealthApi.md#v2healthget) | **GET** /v2/health | Health check endpoint
*InventoryPlanningApi* | [**v2InventoryPlanningPost**](docs/Api/InventoryPlanningApi.md#v2inventoryplanningpost) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations
*TrafficForecastingApi* | [**v2TrafficForecastingPost**](docs/Api/TrafficForecastingApi.md#v2trafficforecastingpost) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations

## Models

- [AnalysisResponse](docs/Model/AnalysisResponse.md)
- [AnalysisResponseMeta](docs/Model/AnalysisResponseMeta.md)
- [AnalysisResponseMetaTiming](docs/Model/AnalysisResponseMetaTiming.md)
- [AnalysisResponseResult](docs/Model/AnalysisResponseResult.md)
- [AnalysisResponseResultCharacteristics](docs/Model/AnalysisResponseResultCharacteristics.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [ForecastRequest](docs/Model/ForecastRequest.md)
- [ForecastRequestDataInner](docs/Model/ForecastRequestDataInner.md)
- [ForecastResponse](docs/Model/ForecastResponse.md)
- [ForecastResponseMeta](docs/Model/ForecastResponseMeta.md)
- [ForecastResponseMetaTiming](docs/Model/ForecastResponseMetaTiming.md)
- [ForecastResponseResult](docs/Model/ForecastResponseResult.md)
- [InventoryPlanningRequest](docs/Model/InventoryPlanningRequest.md)
- [InventoryPlanningRequestDataInner](docs/Model/InventoryPlanningRequestDataInner.md)
- [InventoryPlanningRequestInventorySettings](docs/Model/InventoryPlanningRequestInventorySettings.md)
- [InventoryPlanningRequestInventorySettingsSuppliersInner](docs/Model/InventoryPlanningRequestInventorySettingsSuppliersInner.md)
- [InventoryPlanningResponse](docs/Model/InventoryPlanningResponse.md)
- [InventoryPlanningResponseMeta](docs/Model/InventoryPlanningResponseMeta.md)
- [InventoryPlanningResponseMetaTiming](docs/Model/InventoryPlanningResponseMetaTiming.md)
- [InventoryPlanningResponseResult](docs/Model/InventoryPlanningResponseResult.md)
- [InventoryPlanningResponseResultForecastDataInner](docs/Model/InventoryPlanningResponseResultForecastDataInner.md)
- [InventoryPlanningResponseResultStockAnalysis](docs/Model/InventoryPlanningResponseResultStockAnalysis.md)
- [InventoryPlanningResponseResultSuppliersInner](docs/Model/InventoryPlanningResponseResultSuppliersInner.md)
- [TrafficForecastingRequest](docs/Model/TrafficForecastingRequest.md)
- [TrafficForecastingRequestDataInner](docs/Model/TrafficForecastingRequestDataInner.md)
- [TrafficForecastingRequestTrafficSettings](docs/Model/TrafficForecastingRequestTrafficSettings.md)
- [TrafficForecastingResponse](docs/Model/TrafficForecastingResponse.md)
- [TrafficForecastingResponseMeta](docs/Model/TrafficForecastingResponseMeta.md)
- [TrafficForecastingResponseMetaTiming](docs/Model/TrafficForecastingResponseMetaTiming.md)
- [TrafficForecastingResponseResult](docs/Model/TrafficForecastingResponseResult.md)
- [TrafficForecastingResponseResultCapacityAnalysis](docs/Model/TrafficForecastingResponseResultCapacityAnalysis.md)
- [TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner](docs/Model/TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.md)
- [TrafficForecastingResponseResultCostOptimization](docs/Model/TrafficForecastingResponseResultCostOptimization.md)
- [TrafficForecastingResponseResultCostOptimizationCostBreakdown](docs/Model/TrafficForecastingResponseResultCostOptimizationCostBreakdown.md)
- [TrafficForecastingResponseResultCostOptimizationRecommendationsInner](docs/Model/TrafficForecastingResponseResultCostOptimizationRecommendationsInner.md)
- [TrafficForecastingResponseResultForecastDataInner](docs/Model/TrafficForecastingResponseResultForecastDataInner.md)
- [TrafficForecastingResponseResultScalingRecommendations](docs/Model/TrafficForecastingResponseResultScalingRecommendations.md)
- [TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner](docs/Model/TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.md)
- [TrafficForecastingResponseResultTrafficAlerts](docs/Model/TrafficForecastingResponseResultTrafficAlerts.md)
- [TrafficForecastingResponseResultTrafficAlertsAlertsInner](docs/Model/TrafficForecastingResponseResultTrafficAlertsAlertsInner.md)
- [V1AnyGet404Response](docs/Model/V1AnyGet404Response.md)
- [V2ForecastPost400Response](docs/Model/V2ForecastPost400Response.md)
- [V2Get200Response](docs/Model/V2Get200Response.md)
- [V2HealthGet200Response](docs/Model/V2HealthGet200Response.md)
- [V2InventoryPlanningPost400Response](docs/Model/V2InventoryPlanningPost400Response.md)
- [V2InventoryPlanningPost500Response](docs/Model/V2InventoryPlanningPost500Response.md)
- [V2TrafficForecastingPost500Response](docs/Model/V2TrafficForecastingPost500Response.md)
- [ValidationErrorResponse](docs/Model/ValidationErrorResponse.md)

## Authorization

Authentication schemes defined for the API:
### apiKey

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@forecastapi.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `2.0.0`
    - Package version: `1.0.7`
    - Generator version: `7.16.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
