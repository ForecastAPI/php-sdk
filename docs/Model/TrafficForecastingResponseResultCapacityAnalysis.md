# # TrafficForecastingResponseResultCapacityAnalysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_capacity** | **float** | Current infrastructure capacity | [optional]
**utilization_periods** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner[]**](TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.md) | Capacity utilization for each forecast period | [optional]
**over_capacity_periods** | **int** | Number of periods exceeding capacity | [optional]
**critical_periods** | **int** | Number of periods above 90% utilization | [optional]
**forecast_duration_minutes** | **int** | Total forecast duration in minutes | [optional]
**next_capacity_breach** | **\DateTime** | Date when capacity will be breached | [optional]
**capacity_efficiency** | **float** | Efficiency score (0-100, optimal around 75% utilization) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
