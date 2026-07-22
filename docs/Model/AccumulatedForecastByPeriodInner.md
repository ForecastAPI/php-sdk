# # AccumulatedForecastByPeriodInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **\DateTime** |  | [optional]
**weight** | **float** | survival × discount weight applied to this period (period 1 is 1.0) | [optional]
**cumulative** | **float** | Running weighted total through this period | [optional]
**cumulative_lower** | **float** | Running lower bound; present only when every period so far has a usable band | [optional]
**cumulative_upper** | **float** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
