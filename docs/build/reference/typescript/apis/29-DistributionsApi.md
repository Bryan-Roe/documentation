---
title: Distributions API | TypeScript SDK
---

# Distributions API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**distributionsCreateNewDistribution**](DistributionsApi#distributionscreatenewdistribution) | **POST** /distributions/create | /distributions/create [POST]
[**distributionsDeleteSpecificDistribution**](DistributionsApi#distributionsdeletespecificdistribution) | **POST** /distributions/\{distribution\}/delete | /distributions/\{distribution\}/delete [POST]
[**distributionsSnapshot**](DistributionsApi#distributionssnapshot) | **GET** /distributions | /distributions [GET]


## **distributionsCreateNewDistribution** {#distributionscreatenewdistribution}
> Distribution distributionsCreateNewDistribution()

This will create a new distribution.

### Example {#distributionscreatenewdistribution-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.DistributionsApi(configuration)

const body: Pieces.DistributionsCreateNewDistributionRequest = {
// SeededDistribution |  (optional)
seededDistribution: ,
};

apiInstance.distributionsCreateNewDistribution(body).then((data: Distribution) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#distributionscreatenewdistribution-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededDistribution** | **SeededDistribution**|  |


### Return type {#distributionscreatenewdistribution-return-type}

[**Distribution**](../models/Distribution)

### HTTP request headers {#distributionscreatenewdistribution-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


### HTTP response details {#distributionscreatenewdistribution-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **distributionsDeleteSpecificDistribution** {#distributionsdeletespecificdistribution}
> distributionsDeleteSpecificDistribution()

This will delete a specific distribution.

### Example {#distributionsdeletespecificdistribution-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.DistributionsApi(configuration)

const body: Pieces.DistributionsDeleteSpecificDistributionRequest = {
// string | This is the uuid of a specific distribution.
distribution: distribution_example,
};

apiInstance.distributionsDeleteSpecificDistribution(body).then((data: void (empty response body)) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#distributionsdeletespecificdistribution-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **distribution** | [**string**] | This is the uuid of a specific distribution. | defaults to undefined


### Return type {#distributionsdeletespecificdistribution-return-type}

void (empty response body)

### HTTP request headers {#distributionsdeletespecificdistribution-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: text/plain


### HTTP response details {#distributionsdeletespecificdistribution-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **distributionsSnapshot** {#distributionssnapshot}
> Distributions distributionsSnapshot()

This will get a specific snapshot of all our distributions.

### Example {#distributionssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.DistributionsApi(configuration)

apiInstance.distributionsSnapshot().then((data: Distributions) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#distributionssnapshot-parameters}

This endpoint does not need any parameters.


### Return type {#distributionssnapshot-return-type}

[**Distributions**](../models/Distributions)

### HTTP request headers {#distributionssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


### HTTP response details {#distributionssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |
**500** | Internal Server Error |  -  |


