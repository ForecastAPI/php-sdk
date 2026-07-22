# # GroupedForecastResults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** |  | [optional]
**tenant_context** | **string** |  | [optional]
**hierarchy** | **string[]** |  | [optional]
**reconciliation** | [**\ForecastAPI\Sdk\Model\GroupedForecastResultsReconciliation**](GroupedForecastResultsReconciliation.md) |  | [optional]
**confidence_level** | **float** |  | [optional]
**node_count** | **int** |  | [optional]
**nodes** | [**array<string,\ForecastAPI\Sdk\Model\GroupedForecastNode>**](GroupedForecastNode.md) | Every node of the hierarchy, keyed by segment key: &#x60;total&#x60; for the root, then e.g. &#x60;region&#x3D;eu&#x60; for aggregates and &#x60;plan&#x3D;pro|region&#x3D;eu&#x60; for leaves. Every parent equals the sum of its children in every period. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
