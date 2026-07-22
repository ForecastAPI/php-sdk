# # AnomalyDetectionRequestAllOfAnomalySettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **string** | Detection method; auto picks the best fit for the data&#39;s characteristics | [optional] [default to 'auto']
**threshold** | **float** | Z-score threshold for the zscore method | [optional]
**multiplier** | **float** | IQR multiplier for the iqr method | [optional]
**seasonal_period** | **int** | Season length for the seasonal method; detected automatically when omitted | [optional]
**minimum_periods** | **int** | Minimum data points required before detection runs | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
