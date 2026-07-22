# # ProductInsightsBatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequest[]**](ProductInsightsRequest.md) | One entry per product, each the same shape as a single /v2/product-insights request |
**batch** | **string** | Existing batch identifier to append this upload to, for submitting one logical batch in chunks | [optional]
**parts** | **int** | Total number of parts the batch will consist of, when submitting in chunks | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
