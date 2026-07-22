# # AnomalyDetectionResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anomalies** | [**\ForecastAPI\Sdk\Model\AnomalyDetectionResponseResultAnomaliesInner[]**](AnomalyDetectionResponseResultAnomaliesInner.md) | Detected anomalies, most severe first | [optional]
**analysis** | [**\ForecastAPI\Sdk\Model\AnomalyDetectionResponseResultAnalysis**](AnomalyDetectionResponseResultAnalysis.md) |  | [optional]
**alternatives** | **array<string,mixed>[]** | Other suitable methods (present on auto selection) | [optional]
**statistics** | **array<string,mixed>** | Method statistics (present when a method was named in the request) | [optional]
**interpretation** | **array<string,mixed>** | Human-readable interpretation (present when a method was named in the request) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
