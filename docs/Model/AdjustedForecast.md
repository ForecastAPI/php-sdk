# # AdjustedForecast

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**forecasts** | [**\ForecastAPI\Sdk\Model\ForecastPeriod[]**](ForecastPeriod.md) | The baseline path with every adjustment applied, in array order | [optional]
**adjustments_applied** | [**\ForecastAPI\Sdk\Model\AdjustedForecastAdjustmentsAppliedInner[]**](AdjustedForecastAdjustmentsAppliedInner.md) | Echo of each adjustment as applied, in order | [optional]
**stored** | **bool** | Always false — only the baseline in &#x60;result&#x60; is persisted and scored for accuracy | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
