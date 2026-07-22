# # BatchSeriesResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** |  | [optional]
**tenant_context** | **string** |  | [optional]
**forecasts** | [**\ForecastAPI\Sdk\Model\ForecastPeriod[]**](ForecastPeriod.md) |  | [optional]
**model_info** | **array<string,mixed>** |  | [optional]
**adjusted** | [**\ForecastAPI\Sdk\Model\AdjustedForecast**](AdjustedForecast.md) |  | [optional]
**accumulated** | [**\ForecastAPI\Sdk\Model\AccumulatedForecast**](AccumulatedForecast.md) |  | [optional]
**error** | **string** | Present instead of forecasts when this series failed | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
