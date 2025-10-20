# # TrafficForecastingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **string** | Metric identifier (e.g., endpoint name, service name) |
**frequency** | **string** | Data frequency for forecasting: - M: Minute (for real-time traffic) - H: Hourly - D: Daily - W: Weekly - MS: Monthly (start of month) - ME: Monthly (end of month) - Q: Quarterly - Y: Yearly |
**start_date** | **\DateTime** | Optional start date for the forecast period | [optional]
**periods** | **int** | Number of periods to forecast ahead |
**enable_intelligent_aggregation** | **bool** | Enable intelligent data aggregation for improved forecasting | [optional]
**confidence_level** | **float** | Confidence level for forecast intervals (default 0.95) | [optional]
**data** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingRequestDataInner[]**](TrafficForecastingRequestDataInner.md) | Historical traffic data for forecasting |
**traffic_settings** | [**\ForecastAPI\ForecastSDK\Model\TrafficForecastingRequestTrafficSettings**](TrafficForecastingRequestTrafficSettings.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
