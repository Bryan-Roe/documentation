---
title: Anchors API | TypeScript SDK
---

# Anchors API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**anchorDisassociateAsset**](AnchorsApi#anchordisassociateasset) | **POST** /anchors/\{anchor\}/assets/delete/\{asset\} | /anchors/\{anchor\}/assets/delete/\{asset\} [POST]
[**anchorsCreateNewAnchor**](AnchorsApi#anchorscreatenewanchor) | **POST** /anchors/create | /anchors/create [POST]
[**anchorsDeleteSpecificAnchor**](AnchorsApi#anchorsdeletespecificanchor) | **POST** /anchors/\{anchor\}/delete | /anchors/\{anchor\}/delete [POST]
[**anchorsSnapshot**](AnchorsApi#anchorssnapshot) | **GET** /anchors | /anchors [GET]


## **anchorDisassociateAsset** {#anchordisassociateasset}
> anchorDisassociateAsset()

This will update both the asset and the anchor reference, that will remove a anchor from an asset(only the references).  This will NOT remove the anchor. This will NOT remove the asset. This will only update the references so that they are disconnected from one another.

### Example {#anchordisassociateasset-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnchorsApi(configuration)

const body: Pieces.AnchorDisassociateAssetRequest = {
// string | This is the specific uuid of an anchor.
anchor: anchor_example,
// string | The id (uuid) of the asset that you are trying to access.
asset: 2254f2c8-5797-40e8-ac56-41166dc0e159,
};

apiInstance.anchorDisassociateAsset(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#anchordisassociateasset-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **anchor** | [**string**] | This is the specific uuid of an anchor. | defaults to undefined
 **asset** | [**string**] | The id (uuid) of the asset that you are trying to access. | defaults to undefined


### Return type {#anchordisassociateasset-return-type}

void (empty response body)

### HTTP request headers {#anchordisassociateasset-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#anchordisassociateasset-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **anchorsCreateNewAnchor** {#anchorscreatenewanchor}
> Anchor anchorsCreateNewAnchor()

This will create a anchor and attach it to a specific asset(s) This will also ensure the anchor is normalized.

### Example {#anchorscreatenewanchor-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnchorsApi(configuration)

const body: Pieces.AnchorsCreateNewAnchorRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
// SeededAnchor (optional)
seededAnchor: ,
};

apiInstance.anchorsCreateNewAnchor(body).then((data: Anchor) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#anchorscreatenewanchor-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededAnchor** | **SeededAnchor**|  |
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#anchorscreatenewanchor-return-type}

[**Anchor**](../models/Anchor)

### HTTP request headers {#anchorscreatenewanchor-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#anchorscreatenewanchor-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **anchorsDeleteSpecificAnchor** {#anchorsdeletespecificanchor}
> anchorsDeleteSpecificAnchor()

This will delete a specific anchor!

### Example {#anchorsdeletespecificanchor-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnchorsApi(configuration)

const body: Pieces.AnchorsDeleteSpecificAnchorRequest = {
// string | This is the specific uuid of an anchor.
anchor: anchor_example,
};

apiInstance.anchorsDeleteSpecificAnchor(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#anchorsdeletespecificanchor-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **anchor** | [**string**] | This is the specific uuid of an anchor. | defaults to undefined


### Return type {#anchorsdeletespecificanchor-return-type}

void (empty response body)

### HTTP request headers {#anchorsdeletespecificanchor-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#anchorsdeletespecificanchor-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **anchorsSnapshot** {#anchorssnapshot}
> Anchors anchorsSnapshot()

This will get a snapshot of all your anchors.

### Example {#anchorssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.AnchorsApi(configuration)

const body: Pieces.AnchorsSnapshotRequest = {
// boolean | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) (optional)
transferables: true,
};

apiInstance.anchorsSnapshot(body).then((data: Anchors) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#anchorssnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | [**boolean**] | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | (optional) defaults to undefined


### Return type {#anchorssnapshot-return-type}

[**Anchors**](../models/Anchors)

### HTTP request headers {#anchorssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#anchorssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


