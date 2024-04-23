---
title: Formats API | Dart SDK
---

# Formats API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**formatsSnapshot**](FormatsApi#formatssnapshot) | **GET** /formats | /formats [GET] Scoped to Formats
[**formatsSpecificFormatSnapshot**](FormatsApi#formatsspecificformatsnapshot) | **GET** /formats/\{format\} | /formats/\{format\} [GET] Scoped to Formats


## **formatsSnapshot** {#formatssnapshot}
> Formats formatsSnapshot(transferables)

/formats [GET] Scoped to Formats

Get all of your formats for a given user.

### Example {#formatssnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = FormatsApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.formatsSnapshot(transferables);
    print(result);
} catch (e) {
    print('Exception when calling FormatsApi->formatsSnapshot: $e\n');
}
```

### Parameters {#formatssnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#formatssnapshot-return-type}

[**Formats**](../models/Formats)

### Authorization {#formatssnapshot-authorization}

No authorization required

### HTTP request headers {#formatssnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

## **formatsSpecificFormatSnapshot** {#formatsspecificformatsnapshot}
> Format formatsSpecificFormatSnapshot(format, transferable)

/formats/\{format\} [GET] Scoped to Formats

Request a specific format when given a id (uuid in path params)

### Example {#formatsspecificformatsnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = FormatsApi();
final format = 102ff265-fdfb-4142-8d94-4932d400199c; // String | The id (uuid) for a specific format.
final transferable = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.formatsSpecificFormatSnapshot(format, transferable);
    print(result);
} catch (e) {
    print('Exception when calling FormatsApi->formatsSpecificFormatSnapshot: $e\n');
}
```

### Parameters {#formatsspecificformatsnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **String** | The id (uuid) for a specific format. | 
 **transferable** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#formatsspecificformatsnapshot-return-type}

[**Format**](../models/Format)

### Authorization {#formatsspecificformatsnapshot-authorization}

No authorization required

### HTTP request headers {#formatsspecificformatsnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

