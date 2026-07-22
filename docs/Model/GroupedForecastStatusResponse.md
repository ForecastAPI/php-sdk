# # GroupedForecastStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grouped_forecast_id** | **string** |  | [optional]
**status** | **string** | The run is all-or-nothing — there is no per-node failure state | [optional]
**node_count** | **int** |  | [optional]
**results** | [**\ForecastAPI\Sdk\Model\GroupedForecastResults**](GroupedForecastResults.md) | Populated once status is &#x60;completed&#x60;; null before that and on failure | [optional]
**error** | **string** | Failure reason when status is &#x60;failed&#x60; | [optional]
**started_at** | **\DateTime** |  | [optional]
**completed_at** | **\DateTime** |  | [optional]
**created_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
