# # InventoryPlanningRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | SKU, Product ID, or other identifier for the inventory item |
**frequency** | **string** | Data frequency for forecasting: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly |
**start_date** | **\DateTime** | Optional start date for the forecast period | [optional]
**periods** | **int** | Number of periods to forecast ahead |
**model** | **string** | Forecasting model behind the plan. &#x60;auto&#x60; routes the identifier to whichever model has proven most accurate on it, sharing the scorecard built by /v2/forecast and /v2/batch/forecast; on this endpoint auto&#39;s ensemble default runs as &#x60;standard&#x60; until a winner emerges, and the decision is reported in &#x60;meta.auto_selection&#x60;. Advanced variants, ensemble and auto cost 25% more usage. | [optional] [default to 'standard']
**enable_intelligent_aggregation** | **bool** | Enable intelligent data aggregation for improved forecasting | [optional]
**confidence_level** | **float** | Confidence level for forecast intervals (default 0.95) | [optional]
**data** | [**\ForecastAPI\Sdk\Model\InventoryPlanningRequestDataInner[]**](InventoryPlanningRequestDataInner.md) | Historical demand/sales data for forecasting |
**inventory_settings** | [**\ForecastAPI\Sdk\Model\InventoryPlanningRequestInventorySettings**](InventoryPlanningRequestInventorySettings.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
