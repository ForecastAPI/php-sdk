# # GroupedForecastNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | The measure — the same for every node | [optional]
**segment** | **array<string,mixed>** | The dimension values this node covers — empty for the total, all declared dimensions for a leaf | [optional]
**level** | **int** | Depth in the tree; 0 is the total | [optional]
**is_leaf** | **bool** |  | [optional]
**parent** | **string** | Segment key of the parent node; null for the total | [optional]
**children** | **string[]** | Segment keys of the children; empty for leaves | [optional]
**forecasts** | [**\ForecastAPI\Sdk\Model\ForecastPeriod[]**](ForecastPeriod.md) | The reconciled path — this is what is stored and accuracy-tracked per node | [optional]
**model_info** | **array<string,mixed>** | Method and reconciliation details for this node. With min_trace, the node&#39;s unreconciled path is reported under &#x60;reconciliation.base_forecast&#x60;. When an aggregate band cannot be built honestly (a child&#39;s band coverage is unknown), the band is omitted and &#x60;reconciliation.interval_reason&#x60; states why. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
