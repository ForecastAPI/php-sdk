# # InventoryPlanningRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | SKU, Product ID, or other identifier for the inventory item |
**frequency** | **string** | Data frequency for forecasting: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly |
**start_date** | **\DateTime** | Optional start date for the forecast period | [optional]
**periods** | **int** | Number of periods to forecast ahead |
**enable_intelligent_aggregation** | **bool** | Enable intelligent data aggregation for improved forecasting | [optional]
**confidence_level** | **float** | Confidence level for forecast intervals (default 0.95) | [optional]
**data** | [**\ForecastAPI\ForecastSDK\Model\InventoryPlanningRequestDataInner[]**](InventoryPlanningRequestDataInner.md) | Historical demand/sales data for forecasting |
**inventory_settings** | [**\ForecastAPI\ForecastSDK\Model\InventoryPlanningRequestInventorySettings**](InventoryPlanningRequestInventorySettings.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
