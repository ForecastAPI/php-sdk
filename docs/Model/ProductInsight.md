# # ProductInsight

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**class** | **string** | Insight family (e.g. margin, sales, cost, lead_time) | [optional]
**type** | **string** |  | [optional]
**severity** | **string** |  | [optional]
**title** | **string** |  | [optional]
**description** | **string** |  | [optional]
**metrics** | **array<string,mixed>** | The numbers behind the insight | [optional]
**recommendation** | [**\ForecastAPI\Sdk\Model\ProductInsightRecommendation**](ProductInsightRecommendation.md) |  | [optional]
**confidence** | **string** |  | [optional]
**date** | **string** |  | [optional]
**change_status** | **string** | How this insight compares to the previous analysis of the same product — every insight is \&quot;new\&quot; on the first analysis | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
