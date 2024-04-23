---
title: Metrics API | Python SDK
---

# Metrics API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_metrics_formats**](MetricsApi#get_metrics_formats) | **GET** /metrics/formats | /metrics/formats [GET]
[**metrics_formats_ordered**](MetricsApi#metrics_formats_ordered) | **GET** /metrics/formats/ordered | /metrics/formats/ordered [GET]


## **get_metrics_formats** {#get_metrics_formats}
> FormatsMetrics get_metrics_formats()

/metrics/formats [GET]

This is going to get a snapshot of our FormatsMetrics

### Example {#get_metrics_formats-example}


```python
import pieces_os_client
from pieces_os_client.models.formats_metrics import FormatsMetrics
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
    api_instance = Metrics API(api_client)

    try:
        # /metrics/formats [GET]
        api_response = api_instance.get_metrics_formats()
        print("The response of MetricsApi->get_metrics_formats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->get_metrics_formats: %s\n" % e)
```



### Parameters {#get_metrics_formats-parameters}

This endpoint does not need any parameters.

### Return type {#get_metrics_formats-return-type}

[**FormatsMetrics**](../models/FormatsMetrics)

### Authorization {#get_metrics_formats-authorization}

No authorization required

### HTTP request headers {#get_metrics_formats-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details {#get_metrics_formats-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

## **metrics_formats_ordered** {#metrics_formats_ordered}
> OrderedMetrics metrics_formats_ordered()

/metrics/formats/ordered [GET]

This will return a list of code formats in desc order from most to least formats uploaded.

### Example {#metrics_formats_ordered-example}


```python
import pieces_os_client
from pieces_os_client.models.ordered_metrics import OrderedMetrics
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
    api_instance = Metrics API(api_client)

    try:
        # /metrics/formats/ordered [GET]
        api_response = api_instance.metrics_formats_ordered()
        print("The response of MetricsApi->metrics_formats_ordered:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->metrics_formats_ordered: %s\n" % e)
```



### Parameters {#metrics_formats_ordered-parameters}

This endpoint does not need any parameters.

### Return type {#metrics_formats_ordered-return-type}

[**OrderedMetrics**](../models/OrderedMetrics)

### Authorization {#metrics_formats_ordered-authorization}

No authorization required

### HTTP request headers {#metrics_formats_ordered-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details {#metrics_formats_ordered-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

