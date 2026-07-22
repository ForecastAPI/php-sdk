# # ForecastPeriod

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **int** | 1-based forecast period number | [optional]
**date** | **\DateTime** | Date of this forecast period | [optional]
**forecast** | **float** | Point forecast for this period | [optional]
**lower** | **float** | Lower prediction bound at the requested confidence level | [optional]
**upper** | **float** | Upper prediction bound at the requested confidence level | [optional]
**quantiles** | **array<string,float>** | Present only when &#x60;quantiles&#x60; was requested — the forecast at each requested decile level for this period | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
