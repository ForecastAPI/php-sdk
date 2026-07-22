# # GroupedForecastAccepted

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grouped_forecast_id** | **string** | Id to poll via GET /v2/forecast/grouped/{grouped_forecast_id} | [optional]
**status** | **string** |  | [optional]
**series_count** | **int** | Leaf series submitted | [optional]
**node_count** | **int** | What will actually be forecast and reconciled — the leaves plus every derived aggregate and the total | [optional]
**reconciliation** | **string** |  | [optional]
**time_taken_ms** | **float** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
