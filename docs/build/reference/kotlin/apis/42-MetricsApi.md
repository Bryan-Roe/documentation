# Metrics API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getMetricsFormats**](#getmetricsformats) | **GET** /metrics/formats | /metrics/formats [GET]
[**metricsFormatsOrdered**](#metricsformatsordered) | **GET** /metrics/formats/ordered | /metrics/formats/ordered [GET]


## **getMetricsFormats** {#getmetricsformats}
> FormatsMetrics getMetricsFormats()

/metrics/formats [GET]

This is going to get a snapshot of our FormatsMetrics

### Example
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = MetricsApi()
try {
    val result : FormatsMetrics = apiInstance.getMetricsFormats()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MetricsApi#getMetricsFormats")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MetricsApi#getMetricsFormats")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FormatsMetrics**](../models/FormatsMetrics)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

## **metricsFormatsOrdered** {#metricsformatsordered}
> OrderedMetrics metricsFormatsOrdered()

/metrics/formats/ordered [GET]

This will return a list of code formats in desc order from most to least formats uploaded.

### Example
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = MetricsApi()
try {
    val result : OrderedMetrics = apiInstance.metricsFormatsOrdered()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling MetricsApi#metricsFormatsOrdered")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling MetricsApi#metricsFormatsOrdered")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**OrderedMetrics**](../models/OrderedMetrics)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

