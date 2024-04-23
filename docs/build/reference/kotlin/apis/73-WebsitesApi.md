---
title: Websites API | Kotlin SDK
---

# Websites API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**websitesCreateNewWebsite**](#websitescreatenewwebsite) | **POST** /websites/create | /websites/create [POST]
[**websitesDeleteSpecificWebsite**](#websitesdeletespecificwebsite) | **POST** /websites/\{website\}/delete | /websites/\{website\}/delete [POST]
[**websitesExists**](#websitesexists) | **POST** /websites/exists | /websites/exists [POST]
[**websitesSnapshot**](#websitessnapshot) | **GET** /websites | /websites [GET]


## **websitesCreateNewWebsite** {#websitescreatenewwebsite}
> Website websitesCreateNewWebsite(transferables, seededWebsite)

/websites/create [POST]

This will create a website and attach it to a specific asset.

### Example {#websitescreatenewwebsite-example}
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = Websites API()
val transferables : kotlin.Boolean = true // kotlin.Boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
val seededWebsite : SeededWebsite =  // SeededWebsite | 
try {
    val result : Website = apiInstance.websitesCreateNewWebsite(transferables, seededWebsite)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling Websites API#websitesCreateNewWebsite")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling Websites API#websitesCreateNewWebsite")
    e.printStackTrace()
}
```

### Parameters {#websitescreatenewwebsite-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **kotlin.Boolean**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional]
 **seededWebsite** | [**SeededWebsite**](../models/SeededWebsite)|  | [optional]

### Return type {#websitescreatenewwebsite-return-type}

[**Website**](../models/Website)

### Authorization {#websitescreatenewwebsite-authorization}

No authorization required

### HTTP request headers {#websitescreatenewwebsite-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json

## **websitesDeleteSpecificWebsite** {#websitesdeletespecificwebsite}
> websitesDeleteSpecificWebsite(website)

/websites/\{website\}/delete [POST]

This will delete a specific website!

### Example {#websitesdeletespecificwebsite-example}
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = Websites API()
val website : kotlin.String = website_example // kotlin.String | website id
try {
    apiInstance.websitesDeleteSpecificWebsite(website)
} catch (e: ClientException) {
    println("4xx response calling Websites API#websitesDeleteSpecificWebsite")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling Websites API#websitesDeleteSpecificWebsite")
    e.printStackTrace()
}
```

### Parameters {#websitesdeletespecificwebsite-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **kotlin.String**| website id |

### Return type {#websitesdeletespecificwebsite-return-type}

null (empty response body)

### Authorization {#websitesdeletespecificwebsite-authorization}

No authorization required

### HTTP request headers {#websitesdeletespecificwebsite-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: Not defined

## **websitesExists** {#websitesexists}
> ExistingMetadata websitesExists(existentMetadata)

/websites/exists [POST]

This will check all of the websites in our database to see if this specific provided website actually exists, if not we will just return a null website in the output.

### Example {#websitesexists-example}
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = Websites API()
val existentMetadata : ExistentMetadata =  // ExistentMetadata | 
try {
    val result : ExistingMetadata = apiInstance.websitesExists(existentMetadata)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling Websites API#websitesExists")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling Websites API#websitesExists")
    e.printStackTrace()
}
```

### Parameters {#websitesexists-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **existentMetadata** | [**ExistentMetadata**](../models/ExistentMetadata)|  | [optional]

### Return type {#websitesexists-return-type}

[**ExistingMetadata**](../models/ExistingMetadata)

### Authorization {#websitesexists-authorization}

No authorization required

### HTTP request headers {#websitesexists-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json

## **websitesSnapshot** {#websitessnapshot}
> Websites websitesSnapshot(transferables)

/websites [GET]

This will get a snapshot of all your websites.

### Example {#websitessnapshot-example}
```kotlin
// Import classes:
//import app.pieces.pieces-os-client.infrastructure.*
//import app.pieces.pieces-os-client.models.*

val apiInstance = Websites API()
val transferables : kotlin.Boolean = true // kotlin.Boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
try {
    val result : Websites = apiInstance.websitesSnapshot(transferables)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling Websites API#websitesSnapshot")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling Websites API#websitesSnapshot")
    e.printStackTrace()
}
```

### Parameters {#websitessnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **kotlin.Boolean**| This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional]

### Return type {#websitessnapshot-return-type}

[**Websites**](../models/Websites)

### Authorization {#websitessnapshot-authorization}

No authorization required

### HTTP request headers {#websitessnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

