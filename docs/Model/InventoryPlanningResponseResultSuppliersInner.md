# # InventoryPlanningResponseResultSuppliersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supplier** | **string** | Supplier identifier | [optional]
**order_quantity** | **float** | Recommended order quantity | [optional]
**total_cost** | **float** | Total cost for the recommended order | [optional]
**cost_per_unit** | **float** | Cost per unit from this supplier | [optional]
**expected_delivery** | **\DateTime** | Expected delivery date | [optional]
**lead_time_days** | **float** | Lead time in days | [optional]
**minimum_order_quantity** | **float** | Minimum order quantity | [optional]
**reliability_score** | **float** | Supplier reliability score | [optional]
**lead_time_demand** | **float** | Expected demand during lead time | [optional]
**safety_stock** | **float** | Calculated safety stock for this supplier | [optional]
**reorder_point** | **float** | Calculated reorder point for this supplier | [optional]
**reason** | **string** | Explanation for the recommendation | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
