# # InventoryPlanningResponseResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | Product identifier from the request | [optional]
**current_stock** | **float** | Current stock level | [optional]
**minimum_stock** | **float** | Minimum stock level to maintain | [optional]
**reorder_point** | **float** | Recommended reorder point for optimal supplier | [optional]
**safety_stock** | **float** | Calculated safety stock for optimal supplier | [optional]
**suppliers** | [**\ForecastAPI\Sdk\Model\InventoryPlanningResponseResultSuppliersInner[]**](InventoryPlanningResponseResultSuppliersInner.md) | Analysis and recommendations for each supplier | [optional]
**stock_analysis** | [**\ForecastAPI\Sdk\Model\InventoryPlanningResponseResultStockAnalysis**](InventoryPlanningResponseResultStockAnalysis.md) |  | [optional]
**forecast_data** | [**\ForecastAPI\Sdk\Model\InventoryPlanningResponseResultForecastDataInner[]**](InventoryPlanningResponseResultForecastDataInner.md) | Underlying forecast data used for planning | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
