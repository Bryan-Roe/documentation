---
title: Annotations API | TypeScript SDK
---

# Annotations API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**annotationsCreateNewAnnotation**](AnnotationsApi#annotationscreatenewannotation) | **POST** /annotations/create | /annotations/create [POST]
[**annotationsDeleteSpecificAnnotation**](AnnotationsApi#annotationsdeletespecificannotation) | **POST** /annotations/\{annotation\}/delete | /annotations/\{annotation\}/delete [POST]
[**annotationsSnapshot**](AnnotationsApi#annotationssnapshot) | **GET** /annotations | /annotations [GET]


## **annotationsCreateNewAnnotation** {#annotationscreatenewannotation}
> Annotation annotationsCreateNewAnnotation()

This will create an annotation.

### Example {#annotationscreatenewannotation-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnnotationsApi(configuration)

const body: Pieces.AnnotationsCreateNewAnnotationRequest = {
// SeededAnnotation (optional)
seededAnnotation: ,
};

apiInstance.annotationsCreateNewAnnotation(body).then((data: Annotation) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#annotationscreatenewannotation-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededAnnotation** | **SeededAnnotation**|  |


### Return type {#annotationscreatenewannotation-return-type}

[**Annotation**](../models/Annotation)

### HTTP request headers {#annotationscreatenewannotation-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#annotationscreatenewannotation-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **annotationsDeleteSpecificAnnotation** {#annotationsdeletespecificannotation}
> annotationsDeleteSpecificAnnotation()

this will delete a specific annotation

### Example {#annotationsdeletespecificannotation-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnnotationsApi(configuration)

const body: Pieces.AnnotationsDeleteSpecificAnnotationRequest = {
// string | This is a specific annotation uuid.
annotation: annotation_example,
};

apiInstance.annotationsDeleteSpecificAnnotation(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#annotationsdeletespecificannotation-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation** | [**string**] | This is a specific annotation uuid. | defaults to undefined


### Return type {#annotationsdeletespecificannotation-return-type}

void (empty response body)

### HTTP request headers {#annotationsdeletespecificannotation-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#annotationsdeletespecificannotation-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **annotationsSnapshot** {#annotationssnapshot}
> Annotations annotationsSnapshot()

This will get a snapshot of all the annotations.  This will take an optional filter as a query param.

### Example {#annotationssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnnotationsApi(configuration)

const body: Pieces.AnnotationsSnapshotRequest = {
// 'DESCRIPTION' | 'COMMENT' | 'COMMENTATION' | 'DOCUMENTATION' | 'SUMMARIZATION' | 'SUMMARY' | 'EXPLANATION' | 'GIT_COMMIT' | This is an AnnotationTypeEnum as a optional filter. (optional)
annotationTypeFilter: annotationTypeFilter_example,
};

apiInstance.annotationsSnapshot(body).then((data: Annotations) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#annotationssnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotationTypeFilter** | [**&#39;DESCRIPTION&#39; | &#39;COMMENT&#39; | &#39;COMMENTATION&#39; | &#39;DOCUMENTATION&#39; | &#39;SUMMARIZATION&#39; | &#39;SUMMARY&#39; | &#39;EXPLANATION&#39; | &#39;GIT_COMMIT&#39;**]**Array\<&#39;DESCRIPTION&#39; &#124; &#39;COMMENT&#39; &#124; &#39;COMMENTATION&#39; &#124; &#39;DOCUMENTATION&#39; &#124; &#39;SUMMARIZATION&#39; &#124; &#39;SUMMARY&#39; &#124; &#39;EXPLANATION&#39; &#124; &#39;GIT_COMMIT&#39;\>** | This is an AnnotationTypeEnum as a optional filter. | (optional) defaults to undefined


### Return type {#annotationssnapshot-return-type}

[**Annotations**](../models/Annotations)

### HTTP request headers {#annotationssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#annotationssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


