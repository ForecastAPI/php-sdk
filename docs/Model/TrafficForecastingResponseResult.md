# # TrafficForecastingResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **string** | Metric identifier from the request | [optional]
**current_capacity** | **float** | Current infrastructure capacity | [optional]
**baseline_traffic** | **float** | Baseline traffic level | [optional]
**scaling_recommendations** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultScalingRecommendations**](TrafficForecastingResponseResultScalingRecommendations.md) |  | [optional]
**capacity_analysis** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultCapacityAnalysis**](TrafficForecastingResponseResultCapacityAnalysis.md) |  | [optional]
**traffic_alerts** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultTrafficAlerts**](TrafficForecastingResponseResultTrafficAlerts.md) |  | [optional]
**cost_optimization** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultCostOptimization**](TrafficForecastingResponseResultCostOptimization.md) |  | [optional]
**forecast_data** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultForecastDataInner[]**](TrafficForecastingResponseResultForecastDataInner.md) | Underlying forecast data used for analysis | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
