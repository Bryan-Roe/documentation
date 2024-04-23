---
title: Hints API | Python SDK
---

# Hints API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**hints_create_new_hint**](HintsApi#hints_create_new_hint) | **POST** /hints/create | /hints/create [POST]
[**hints_delete_specific_hint**](HintsApi#hints_delete_specific_hint) | **POST** /hints/\{hint\}/delete | /hints/\{hint\}/delete [POST]
[**hints_snapshot**](HintsApi#hints_snapshot) | **GET** /hints | /hints [GET]


## **hints_create_new_hint** {#hints_create_new_hint}
> Hint hints_create_new_hint(seeded_hint=seeded_hint)

/hints/create [POST]

This will create a hint.

### Example {#hints_create_new_hint-example}


```python
import pieces_os_client
from pieces_os_client.models.hint import Hint
from pieces_os_client.models.seeded_hint import SeededHint
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host = "http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = Hints API(api_client)
    seeded_hint = pieces_os_client.SeededHint() # SeededHint |  (optional)

    try:
        # /hints/create [POST]
        api_response = api_instance.hints_create_new_hint(seeded_hint=seeded_hint)
        print("The response of HintsApi->hints_create_new_hint:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HintsApi->hints_create_new_hint: %s\n" % e)
```



### Parameters {#hints_create_new_hint-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seeded_hint** | [**SeededHint**](../models/SeededHint)|  | [optional] 

### Return type {#hints_create_new_hint-return-type}

[**Hint**](../models/Hint)

### Authorization {#hints_create_new_hint-authorization}

No authorization required

### HTTP request headers {#hints_create_new_hint-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#hints_create_new_hint-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

## **hints_delete_specific_hint** {#hints_delete_specific_hint}
> hints_delete_specific_hint(hint)

/hints/\{hint\}/delete [POST]

This will delete a specific hint.

### Example {#hints_delete_specific_hint-example}


```python
import pieces_os_client
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host = "http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = Hints API(api_client)
    hint = 'hint_example' # str | This is a specific hint uuid

    try:
        # /hints/\{hint\}/delete [POST]
        api_instance.hints_delete_specific_hint(hint)
    except Exception as e:
        print("Exception when calling HintsApi->hints_delete_specific_hint: %s\n" % e)
```



### Parameters {#hints_delete_specific_hint-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hint** | **str**| This is a specific hint uuid | 

### Return type {#hints_delete_specific_hint-return-type}

void (empty response body)

### Authorization {#hints_delete_specific_hint-authorization}

No authorization required

### HTTP request headers {#hints_delete_specific_hint-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain


### HTTP response details {#hints_delete_specific_hint-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**500** | Internal Server Error |  -  |

## **hints_snapshot** {#hints_snapshot}
> Hints hints_snapshot()

/hints [GET]

This will get a snapshot of all of the hints.

### Example {#hints_snapshot-example}


```python
import pieces_os_client
from pieces_os_client.models.hints import Hints
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host = "http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = Hints API(api_client)

    try:
        # /hints [GET]
        api_response = api_instance.hints_snapshot()
        print("The response of HintsApi->hints_snapshot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HintsApi->hints_snapshot: %s\n" % e)
```



### Parameters {#hints_snapshot-parameters}

This endpoint does not need any parameters.

### Return type {#hints_snapshot-return-type}

[**Hints**](../models/Hints)

### Authorization {#hints_snapshot-authorization}

No authorization required

### HTTP request headers {#hints_snapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain


### HTTP response details {#hints_snapshot-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**500** | Internal Server Error |  -  |

