---
title: Hints API | TypeScript SDK
---

# Hints API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**hintsCreateNewHint**](HintsApi#hintscreatenewhint) | **POST** /hints/create | /hints/create [POST]
[**hintsDeleteSpecificHint**](HintsApi#hintsdeletespecifichint) | **POST** /hints/\{hint\}/delete | /hints/\{hint\}/delete [POST]
[**hintsSnapshot**](HintsApi#hintssnapshot) | **GET** /hints | /hints [GET]


## **hintsCreateNewHint** {#hintscreatenewhint}
> Hint hintsCreateNewHint()

This will create a hint.

### Example {#hintscreatenewhint-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.HintsApi(configuration)

const body: Pieces.HintsCreateNewHintRequest = {
// SeededHint (optional)
seededHint: ,
};

apiInstance.hintsCreateNewHint(body).then((data: Hint) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#hintscreatenewhint-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededHint** | **SeededHint**|  |


### Return type {#hintscreatenewhint-return-type}

[**Hint**](../models/Hint)

### HTTP request headers {#hintscreatenewhint-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#hintscreatenewhint-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **hintsDeleteSpecificHint** {#hintsdeletespecifichint}
> hintsDeleteSpecificHint()

This will delete a specific hint.

### Example {#hintsdeletespecifichint-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.HintsApi(configuration)

const body: Pieces.HintsDeleteSpecificHintRequest = {
// string | This is a specific hint uuid
hint: hint_example,
};

apiInstance.hintsDeleteSpecificHint(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#hintsdeletespecifichint-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hint** | [**string**] | This is a specific hint uuid | defaults to undefined


### Return type {#hintsdeletespecifichint-return-type}

void (empty response body)

### HTTP request headers {#hintsdeletespecifichint-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#hintsdeletespecifichint-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **hintsSnapshot** {#hintssnapshot}
> Hints hintsSnapshot()

This will get a snapshot of all of the hints.

### Example {#hintssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.HintsApi(configuration)

apiInstance.hintsSnapshot().then((data: Hints) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#hintssnapshot-parameters}

This endpoint does not need any parameters.


### Return type {#hintssnapshot-return-type}

[**Hints**](../models/Hints)

### HTTP request headers {#hintssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#hintssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


