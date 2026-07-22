# # AccumulatedForecast

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **float** | Σ (value × survival × discount) over the horizon. Null when a period lacks a usable point forecast (see &#x60;total_reason&#x60;). | [optional]
**total_reason** | **string** | Why &#x60;total&#x60; is null; null when the total is usable | [optional]
**lower** | **float** | Lower bound of the total under the stated correlation assumption. Null with an &#x60;interval_reason&#x60; when any period lacks a band or its coverage is unknown — rather than a band built from a partial set of variances. | [optional]
**upper** | **float** |  | [optional]
**interval_reason** | **string** | Why the total&#39;s band is absent; null when the band is present | [optional]
**confidence_level** | **float** | Coverage the total&#39;s band targets | [optional]
**path** | **string** | Which path was accumulated — &#x60;adjusted&#x60; when &#x60;adjustments&#x60; was also sent, otherwise &#x60;baseline&#x60; | [optional]
**assumptions** | [**\ForecastAPI\Sdk\Model\AccumulatedForecastAssumptions**](AccumulatedForecastAssumptions.md) |  | [optional]
**by_period** | [**\ForecastAPI\Sdk\Model\AccumulatedForecastByPeriodInner[]**](AccumulatedForecastByPeriodInner.md) | Running accumulation per period — &#x60;cumulative&#x60; through period L is the number a lead-time/safety-stock calculation reads | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
