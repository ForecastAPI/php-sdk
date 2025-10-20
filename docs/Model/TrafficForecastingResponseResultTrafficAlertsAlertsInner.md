# # TrafficForecastingResponseResultTrafficAlertsAlertsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Type of alert | [optional]
**severity** | **string** | Alert severity | [optional]
**period** | **int** | Period number where alert occurs | [optional]
**date** | **\DateTime** | Date/time of the alert | [optional]
**predicted_traffic** | **float** | Predicted traffic value | [optional]
**baseline_traffic** | **float** | Baseline traffic (for spikes) | [optional]
**increase_factor** | **float** | Traffic increase factor (for spikes) | [optional]
**z_score** | **float** | Z-score for anomaly detection | [optional]
**message** | **string** | Alert message | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
