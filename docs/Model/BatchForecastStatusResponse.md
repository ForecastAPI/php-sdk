# # BatchForecastStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | The batch id | [optional]
**status** | **string** |  | [optional]
**batch_parts** | **int** | Number of parts the batch was split into for processing | [optional]
**results** | [**\ForecastAPI\Sdk\Model\BatchForecastStatusResponseResults**](BatchForecastStatusResponseResults.md) |  | [optional]
**parts** | [**\ForecastAPI\Sdk\Model\BatchForecastStatusResponsePartsInner[]**](BatchForecastStatusResponsePartsInner.md) | Per-part progress metadata (the forecasts themselves live under results.data) | [optional]
**started_at** | **\DateTime** |  | [optional]
**completed_at** | **\DateTime** |  | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
