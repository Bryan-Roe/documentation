---
title: OCRAnalyses API | Dart SDK
---

# OCRAnalyses API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**ocrAnalysesSnapshot**](OCRAnalysesApi#ocranalysessnapshot) | **GET** /ocr_analyses | Your GET endpoint


## **ocrAnalysesSnapshot** {#ocranalysessnapshot}
> OCRAnalyses ocrAnalysesSnapshot(transferables)

Your GET endpoint

This will get a snapshot of all of your ocr analyses, an ocr analysis is attached to an image analysis.

### Example {#ocranalysessnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OCRAnalysesApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.ocrAnalysesSnapshot(transferables);
    print(result);
} catch (e) {
    print('Exception when calling OCRAnalysesApi->ocrAnalysesSnapshot: $e\n');
}
```

### Parameters {#ocranalysessnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#ocranalysessnapshot-return-type}

[**OCRAnalyses**](../models/OCRAnalyses)

### Authorization {#ocranalysessnapshot-authorization}

No authorization required

### HTTP request headers {#ocranalysessnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

