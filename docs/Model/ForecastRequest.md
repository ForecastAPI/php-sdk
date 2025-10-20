# # ForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | SKU, Product ID, or other identifier for the data series |
**frequency** | **string** | Data frequency: - D: Daily - W: Weekly - M: Monthly (end of month) - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly |
**start_date** | **\DateTime** | Optional start date for the forecast | [optional]
**data_type** | **string** | Type of data (e.g., sales, demand, inventory, web_traffic) |
**periods** | **int** | Number of periods to forecast |
**data** | [**\ForecastAPI\ForecastSDK\Model\ForecastRequestDataInner[]**](ForecastRequestDataInner.md) | Historical time series data |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
