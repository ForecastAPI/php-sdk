# ForecastAPI\ForecastSDK\HealthApi

All URIs are relative to https://forecastapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v2Get()**](HealthApi.md#v2Get) | **GET** /v2 | API root endpoint |
| [**v2HealthGet()**](HealthApi.md#v2HealthGet) | **GET** /v2/health | Health check endpoint |


## `v2Get()`

```php
v2Get(): \ForecastAPI\ForecastSDK\Model\V2Get200Response
```

API root endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ForecastAPI\ForecastSDK\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->v2Get();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->v2Get: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ForecastAPI\ForecastSDK\Model\V2Get200Response**](../Model/V2Get200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v2HealthGet()`

```php
v2HealthGet(): \ForecastAPI\ForecastSDK\Model\V2HealthGet200Response
```

Health check endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new ForecastAPI\ForecastSDK\Api\HealthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->v2HealthGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling HealthApi->v2HealthGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\ForecastAPI\ForecastSDK\Model\V2HealthGet200Response**](../Model/V2HealthGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
