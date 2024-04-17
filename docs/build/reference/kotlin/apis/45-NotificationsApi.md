# Notifications API

All URIs are relative to *http://localhost:1000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sendLocalNotification**](#sendlocalnotification) | **POST** /notifications/local/send | Send notification


## **sendLocalNotification** {#sendlocalnotification}
> sendLocalNotification(notification)

Send notification

Retrieves a snapshot of all available models.

### Example
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = NotificationsApi()
val notification : Notification =  // Notification | 
try {
    apiInstance.sendLocalNotification(notification)
} catch (e: ClientException) {
    println("4xx response calling NotificationsApi#sendLocalNotification")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NotificationsApi#sendLocalNotification")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **notification** | [**Notification**](../models/Notification)|  | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

