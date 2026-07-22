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
      "url": "https://github.com/ForecastAPI/php-sdk.git"
    }
  ],
  "require": {
    "ForecastAPI/php-sdk": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: apiKey
$config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ForecastAPI\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new ForecastAPI\Sdk\Api\AnalysisApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forecast_request = new \ForecastAPI\Sdk\Model\ForecastRequest(); // \ForecastAPI\Sdk\Model\ForecastRequest

try {
    $result = $apiInstance->analyzeTimeSeries($forecast_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AnalysisApi->analyzeTimeSeries: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://forecastapi.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalysisApi* | [**analyzeTimeSeries**](docs/Api/AnalysisApi.md#analyzetimeseries) | **POST** /v2/analyze | Analyze time series data without generating forecast
*AnomalyDetectionApi* | [**detectAnomalies**](docs/Api/AnomalyDetectionApi.md#detectanomalies) | **POST** /v2/detect-anomalies | Detect anomalies in time series data
*BatchForecastingApi* | [**createBatchForecast**](docs/Api/BatchForecastingApi.md#createbatchforecast) | **POST** /v2/batch/forecast | Submit a batch of series for forecasting
*BatchForecastingApi* | [**getBatchForecast**](docs/Api/BatchForecastingApi.md#getbatchforecast) | **GET** /v2/batch/forecast/{batch_id} | Poll a batch forecast for status and results
*BatchForecastingApi* | [**presignBatchForecast**](docs/Api/BatchForecastingApi.md#presignbatchforecast) | **POST** /v2/batch/forecast/presign | Get a presigned URL for a file-based batch upload
*ForecastingApi* | [**createForecast**](docs/Api/ForecastingApi.md#createforecast) | **POST** /v2/forecast | Generate forecast for time series data
*GroupedForecastingApi* | [**createGroupedForecast**](docs/Api/GroupedForecastingApi.md#creategroupedforecast) | **POST** /v2/forecast/grouped | Submit a grouped (hierarchical) forecast with reconciliation
*GroupedForecastingApi* | [**getGroupedForecast**](docs/Api/GroupedForecastingApi.md#getgroupedforecast) | **GET** /v2/forecast/grouped/{grouped_forecast_id} | Poll a grouped forecast for status and results
*HealthApi* | [**getApiRoot**](docs/Api/HealthApi.md#getapiroot) | **GET** /v2 | API root endpoint
*HealthApi* | [**healthCheck**](docs/Api/HealthApi.md#healthcheck) | **GET** /v2/health | Health check endpoint
*InventoryPlanningApi* | [**createInventoryPlan**](docs/Api/InventoryPlanningApi.md#createinventoryplan) | **POST** /v2/inventory-planning | Generate comprehensive inventory planning recommendations
*ProductInsightsApi* | [**createBatchProductInsights**](docs/Api/ProductInsightsApi.md#createbatchproductinsights) | **POST** /v2/batch/product-insights | Submit a batch of products for insights analysis
*ProductInsightsApi* | [**createProductInsights**](docs/Api/ProductInsightsApi.md#createproductinsights) | **POST** /v2/product-insights | Analyze product performance for anomalies, trends and business insights
*ProductInsightsApi* | [**getProductInsightsBatch**](docs/Api/ProductInsightsApi.md#getproductinsightsbatch) | **GET** /v2/batch/product-insights/{batch_id} | Poll a product insights batch for status and results
*TrafficForecastingApi* | [**createTrafficForecast**](docs/Api/TrafficForecastingApi.md#createtrafficforecast) | **POST** /v2/traffic-forecasting | Generate traffic forecasting with infrastructure scaling recommendations

## Models

- [AccumulateOptions](docs/Model/AccumulateOptions.md)
- [AccumulatedForecast](docs/Model/AccumulatedForecast.md)
- [AccumulatedForecastAssumptions](docs/Model/AccumulatedForecastAssumptions.md)
- [AccumulatedForecastByPeriodInner](docs/Model/AccumulatedForecastByPeriodInner.md)
- [AdjustedForecast](docs/Model/AdjustedForecast.md)
- [AdjustedForecastAdjustmentsAppliedInner](docs/Model/AdjustedForecastAdjustmentsAppliedInner.md)
- [AdjustmentsInner](docs/Model/AdjustmentsInner.md)
- [AnalysisResponse](docs/Model/AnalysisResponse.md)
- [AnalysisResponseMeta](docs/Model/AnalysisResponseMeta.md)
- [AnalysisResponseMetaTiming](docs/Model/AnalysisResponseMetaTiming.md)
- [AnalysisResponseResult](docs/Model/AnalysisResponseResult.md)
- [AnalysisResponseResultCharacteristics](docs/Model/AnalysisResponseResultCharacteristics.md)
- [AnomalyDetectionRequest](docs/Model/AnomalyDetectionRequest.md)
- [AnomalyDetectionRequestAllOfAnomalySettings](docs/Model/AnomalyDetectionRequestAllOfAnomalySettings.md)
- [AnomalyDetectionResponse](docs/Model/AnomalyDetectionResponse.md)
- [AnomalyDetectionResponseMeta](docs/Model/AnomalyDetectionResponseMeta.md)
- [AnomalyDetectionResponseMetaTiming](docs/Model/AnomalyDetectionResponseMetaTiming.md)
- [AnomalyDetectionResponseResult](docs/Model/AnomalyDetectionResponseResult.md)
- [AnomalyDetectionResponseResultAnalysis](docs/Model/AnomalyDetectionResponseResultAnalysis.md)
- [AnomalyDetectionResponseResultAnalysisDetectionSummary](docs/Model/AnomalyDetectionResponseResultAnalysisDetectionSummary.md)
- [AnomalyDetectionResponseResultAnomaliesInner](docs/Model/AnomalyDetectionResponseResultAnomaliesInner.md)
- [BatchForecastAccepted](docs/Model/BatchForecastAccepted.md)
- [BatchForecastRequest](docs/Model/BatchForecastRequest.md)
- [BatchForecastSeries](docs/Model/BatchForecastSeries.md)
- [BatchForecastSeriesDataInner](docs/Model/BatchForecastSeriesDataInner.md)
- [BatchForecastStatusResponse](docs/Model/BatchForecastStatusResponse.md)
- [BatchForecastStatusResponsePartsInner](docs/Model/BatchForecastStatusResponsePartsInner.md)
- [BatchForecastStatusResponseResults](docs/Model/BatchForecastStatusResponseResults.md)
- [BatchForecastStatusResponseResultsSummary](docs/Model/BatchForecastStatusResponseResultsSummary.md)
- [BatchPresignResponse](docs/Model/BatchPresignResponse.md)
- [BatchSeriesResult](docs/Model/BatchSeriesResult.md)
- [CreateBatchProductInsights422Response](docs/Model/CreateBatchProductInsights422Response.md)
- [CreateBatchProductInsights500Response](docs/Model/CreateBatchProductInsights500Response.md)
- [CreateForecast400Response](docs/Model/CreateForecast400Response.md)
- [CreateForecast502Response](docs/Model/CreateForecast502Response.md)
- [CreateInventoryPlan400Response](docs/Model/CreateInventoryPlan400Response.md)
- [CreateInventoryPlan500Response](docs/Model/CreateInventoryPlan500Response.md)
- [CreateProductInsights400Response](docs/Model/CreateProductInsights400Response.md)
- [CreateTrafficForecast500Response](docs/Model/CreateTrafficForecast500Response.md)
- [DetectAnomalies422Response](docs/Model/DetectAnomalies422Response.md)
- [DetectAnomalies422ResponseOneOf](docs/Model/DetectAnomalies422ResponseOneOf.md)
- [DetectAnomalies500Response](docs/Model/DetectAnomalies500Response.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [ForecastPeriod](docs/Model/ForecastPeriod.md)
- [ForecastRequest](docs/Model/ForecastRequest.md)
- [ForecastRequestDataInner](docs/Model/ForecastRequestDataInner.md)
- [ForecastResponse](docs/Model/ForecastResponse.md)
- [ForecastResponseMeta](docs/Model/ForecastResponseMeta.md)
- [ForecastResponseMetaTiming](docs/Model/ForecastResponseMetaTiming.md)
- [ForecastResponseResult](docs/Model/ForecastResponseResult.md)
- [GetApiRoot200Response](docs/Model/GetApiRoot200Response.md)
- [GetGroupedForecast404Response](docs/Model/GetGroupedForecast404Response.md)
- [GroupedForecastAccepted](docs/Model/GroupedForecastAccepted.md)
- [GroupedForecastNode](docs/Model/GroupedForecastNode.md)
- [GroupedForecastRequest](docs/Model/GroupedForecastRequest.md)
- [GroupedForecastResults](docs/Model/GroupedForecastResults.md)
- [GroupedForecastResultsReconciliation](docs/Model/GroupedForecastResultsReconciliation.md)
- [GroupedForecastSeries](docs/Model/GroupedForecastSeries.md)
- [GroupedForecastSeriesDataInner](docs/Model/GroupedForecastSeriesDataInner.md)
- [GroupedForecastStatusResponse](docs/Model/GroupedForecastStatusResponse.md)
- [HealthCheck200Response](docs/Model/HealthCheck200Response.md)
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
- [ProductInsight](docs/Model/ProductInsight.md)
- [ProductInsightRecommendation](docs/Model/ProductInsightRecommendation.md)
- [ProductInsightsBatchRequest](docs/Model/ProductInsightsBatchRequest.md)
- [ProductInsightsBatchStatusResponse](docs/Model/ProductInsightsBatchStatusResponse.md)
- [ProductInsightsRequest](docs/Model/ProductInsightsRequest.md)
- [ProductInsightsRequestBaselinePeriodDays](docs/Model/ProductInsightsRequestBaselinePeriodDays.md)
- [ProductInsightsRequestCostHistoryInner](docs/Model/ProductInsightsRequestCostHistoryInner.md)
- [ProductInsightsRequestInsightSettings](docs/Model/ProductInsightsRequestInsightSettings.md)
- [ProductInsightsRequestPurchasesInner](docs/Model/ProductInsightsRequestPurchasesInner.md)
- [ProductInsightsRequestSalesInner](docs/Model/ProductInsightsRequestSalesInner.md)
- [ProductInsightsResponse](docs/Model/ProductInsightsResponse.md)
- [ProductInsightsResponseMeta](docs/Model/ProductInsightsResponseMeta.md)
- [ProductInsightsResponseMetaDataQuality](docs/Model/ProductInsightsResponseMetaDataQuality.md)
- [ProductInsightsResponseMetaTiming](docs/Model/ProductInsightsResponseMetaTiming.md)
- [ProductInsightsResponseResult](docs/Model/ProductInsightsResponseResult.md)
- [ProductInsightsResponseResultComparison](docs/Model/ProductInsightsResponseResultComparison.md)
- [ProductInsightsResponseResultComparisonDevelopments](docs/Model/ProductInsightsResponseResultComparisonDevelopments.md)
- [ProductInsightsResponseResultProductInfo](docs/Model/ProductInsightsResponseResultProductInfo.md)
- [ProductInsightsResponseResultSummary](docs/Model/ProductInsightsResponseResultSummary.md)
- [ProductInsightsResponseResultSummaryAnalysisPeriod](docs/Model/ProductInsightsResponseResultSummaryAnalysisPeriod.md)
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
- [ValidationErrorResponse](docs/Model/ValidationErrorResponse.md)
- [ValidationFailedResponse](docs/Model/ValidationFailedResponse.md)
- [ValueBounds](docs/Model/ValueBounds.md)

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

- API version: `2.0.4`
    - Generator version: `7.16.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
