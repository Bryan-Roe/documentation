---
title: Model API | TypeScript SDK
---

# Model API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**modelSpecificModelDownload**](ModelApi#modelspecificmodeldownload) | **POST** /model/\{model\}/download | /model/\{model\}/download [POST]
[**modelSpecificModelDownloadCancel**](ModelApi#modelspecificmodeldownloadcancel) | **POST** /model/\{model\}/download/cancel | /model/\{model\}/download/cancel [POST]
[**modelSpecificModelDownloadProgress**](ModelApi#modelspecificmodeldownloadprogress) | **GET** /model/\{model\}/download/progress | /model/\{model\}/download/progress [WS]
[**modelSpecificModelLoad**](ModelApi#modelspecificmodelload) | **POST** /model/\{model\}/load | /model/\{model\}/load [POST]
[**modelSpecificModelUnload**](ModelApi#modelspecificmodelunload) | **POST** /model/\{model\}/unload | /model/\{model\}/unload [POST]
[**modelUpdate**](ModelApi#modelupdate) | **POST** /model/update | /model/update [POST]
[**modelsSpecificModelSnapshot**](ModelApi#modelsspecificmodelsnapshot) | **GET** /model/\{model\} | /model/\{model\} [GET]


## **modelSpecificModelDownload** {#modelspecificmodeldownload}
> Model modelSpecificModelDownload()

Downloads a specific model to your local machine.

### Example {#modelspecificmodeldownload-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelSpecificModelDownloadRequest = {
// string | model id
model: model_example,
};

apiInstance.modelSpecificModelDownload(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelspecificmodeldownload-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelspecificmodeldownload-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelspecificmodeldownload-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelspecificmodeldownload-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelSpecificModelDownloadCancel** {#modelspecificmodeldownloadcancel}
> Model modelSpecificModelDownloadCancel()

Cancels a specific model download that is currently in progress.

### Example {#modelspecificmodeldownloadcancel-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelSpecificModelDownloadCancelRequest = {
// string | model id
model: model_example,
};

apiInstance.modelSpecificModelDownloadCancel(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelspecificmodeldownloadcancel-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelspecificmodeldownloadcancel-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelspecificmodeldownloadcancel-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelspecificmodeldownloadcancel-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelSpecificModelDownloadProgress** {#modelspecificmodeldownloadprogress}
> ModelDownloadProgress modelSpecificModelDownloadProgress()

This is a WebSocket connection that provides real-time updates on the download progress of a specific model.

### Example {#modelspecificmodeldownloadprogress-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelSpecificModelDownloadProgressRequest = {
// string | model id
model: model_example,
};

apiInstance.modelSpecificModelDownloadProgress(body).then((data: ModelDownloadProgress) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelspecificmodeldownloadprogress-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelspecificmodeldownloadprogress-return-type}

[**ModelDownloadProgress**](../models/ModelDownloadProgress)

### HTTP request headers {#modelspecificmodeldownloadprogress-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelspecificmodeldownloadprogress-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelSpecificModelLoad** {#modelspecificmodelload}
> Model modelSpecificModelLoad()

Loads a previously downloaded model into memory. It differs from downloading, as downloading involves transferring the entire model to your machine, while loading simply loads the model into memory.

### Example {#modelspecificmodelload-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelSpecificModelLoadRequest = {
// string | model id
model: model_example,
};

apiInstance.modelSpecificModelLoad(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelspecificmodelload-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelspecificmodelload-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelspecificmodelload-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelspecificmodelload-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelSpecificModelUnload** {#modelspecificmodelunload}
> Model modelSpecificModelUnload()

Unloads a previously loaded model from memory and effectively frees up the RAM consumed by the model.

### Example {#modelspecificmodelunload-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelSpecificModelUnloadRequest = {
// string | model id
model: model_example,
};

apiInstance.modelSpecificModelUnload(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelspecificmodelunload-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelspecificmodelunload-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelspecificmodelunload-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelspecificmodelunload-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelUpdate** {#modelupdate}
> Model modelUpdate()

Updates a machine learning model. This functionality is exclusively available for models with the \'custom:true\' setting.

### Example {#modelupdate-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelUpdateRequest = {
// Model (optional)
model: ,
};

apiInstance.modelUpdate(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelupdate-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **Model**|  |


### Return type {#modelupdate-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelupdate-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#modelupdate-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **modelsSpecificModelSnapshot** {#modelsspecificmodelsnapshot}
> Model modelsSpecificModelSnapshot()

Retrieves a specific ML model.

### Example {#modelsspecificmodelsnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.ModelApi(configuration)

const body: Pieces.ModelsSpecificModelSnapshotRequest = {
// string | model id
model: model_example,
};

apiInstance.modelsSpecificModelSnapshot(body).then((data: Model) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#modelsspecificmodelsnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | [**string**] | model id | defaults to undefined


### Return type {#modelsspecificmodelsnapshot-return-type}

[**Model**](../models/Model)

### HTTP request headers {#modelsspecificmodelsnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#modelsspecificmodelsnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**410** | model was not found. |  -  |


