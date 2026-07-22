# # ProductInsightsBatchStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | The batch id | [optional]
**status** | **string** |  | [optional]
**batch_parts** | **int** |  | [optional]
**results** | **array<string,mixed>** | Summary and per-product analysis results as parts complete | [optional]
**parts** | **array<string,mixed>[]** | Per-part progress, each carrying its analyses once processed | [optional]
**started_at** | **\DateTime** |  | [optional]
**completed_at** | **\DateTime** |  | [optional]
**created_at** | **\DateTime** |  | [optional]
**updated_at** | **\DateTime** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
