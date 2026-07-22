# # ProductInsightsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | Product identifier |
**tenant_context** | **string** |  | [optional]
**product_name** | **string** |  | [optional]
**product_group_id** | **string** |  | [optional]
**base_currency** | **string** | ISO 4217 currency the analysis reports in | [optional]
**baseline_period_days** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequestBaselinePeriodDays**](ProductInsightsRequestBaselinePeriodDays.md) |  | [optional]
**locale** | **string** | Locale for insight texts | [optional] [default to 'en']
**sales** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequestSalesInner[]**](ProductInsightsRequestSalesInner.md) |  | [optional]
**purchases** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequestPurchasesInner[]**](ProductInsightsRequestPurchasesInner.md) |  | [optional]
**cost_history** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequestCostHistoryInner[]**](ProductInsightsRequestCostHistoryInner.md) |  | [optional]
**insight_settings** | [**\ForecastAPI\Sdk\Model\ProductInsightsRequestInsightSettings**](ProductInsightsRequestInsightSettings.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
