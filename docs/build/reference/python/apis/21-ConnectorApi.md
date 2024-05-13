---
title: Connector API | Python SDK
---

# Connector API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**connect**](ConnectorApi#connect) | **POST** /connect | /connect [POST]
[**intention**](ConnectorApi#intention) | **POST** /\{application\}/intention | /\{application\}/intention [POST]
[**onboarded**](ConnectorApi#onboarded) | **POST** /\{application\}/onboarded | /onboarded [POST]
[**react**](ConnectorApi#react) | **POST** /\{application\}/reaction | /\{application\}/reaction [POST]
[**suggest**](ConnectorApi#suggest) | **POST** /\{application\}/suggestion | /\{application\}/suggestion [POST]
[**track**](ConnectorApi#track) | **POST** /\{application\}/track | /\{application\}/track [POST]


## **connect** {#connect}
> Context connect(seeded_connector_connection=seeded_connector_connection)

/connect [POST]

Abstracts a bootup/connection for a specific context.

### Example {#connect-example}


```python
import pieces_os_client
from pieces_os_client.models.context import Context
from pieces_os_client.models.seeded_connector_connection import SeededConnectorConnection
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    seeded_connector_connection = pieces_os_client.SeededConnectorConnection() # SeededConnectorConnection |  (optional)

    try:
        # /connect [POST]
        api_response = api_instance.connect(seeded_connector_connection=seeded_connector_connection)
        print("The response of ConnectorApi->connect:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->connect: %s\n" % e)
```



### Parameters {#connect-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seeded_connector_connection** | [**SeededConnectorConnection**](../models/SeededConnectorConnection)|  | [optional] 

### Return type {#connect-return-type}

[**Context**](../models/Context)

### Authorization {#connect-authorization}

No authorization required

### HTTP request headers {#connect-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#connect-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |

## **intention** {#intention}
> str intention(application, seeded_connector_asset=seeded_connector_asset)

/\{application\}/intention [POST]

Allows you to send a SeededAsset for future comparison.

### Example {#intention-example}


```python
import pieces_os_client
from pieces_os_client.models.seeded_connector_asset import SeededConnectorAsset
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    application = 'application_example' # str | 
    seeded_connector_asset = pieces_os_client.SeededConnectorAsset() # SeededConnectorAsset |  (optional)

    try:
        # /\{application\}/intention [POST]
        api_response = api_instance.intention(application, seeded_connector_asset=seeded_connector_asset)
        print("The response of ConnectorApi->intention:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->intention: %s\n" % e)
```



### Parameters {#intention-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **str**|  | 
 **seeded_connector_asset** | [**SeededConnectorAsset**](../models/SeededConnectorAsset)|  | [optional] 

### Return type {#intention-return-type}

**str**

### Authorization {#intention-authorization}

No authorization required

### HTTP request headers {#intention-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain


### HTTP response details {#intention-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |
**401** | Unauthorized, you will get this in the case that you are trying to ping Pieces_OS but havnt connected yet.\&quot;/connect was not called for your application.\&quot; |  -  |
**500** | Internal Server Error:  |  -  |

## **onboarded** {#onboarded}
> str onboarded(application, body=body)

/onboarded [POST]

A central endpoint to manage updates to the onboarding process.

### Example {#onboarded-example}


```python
import pieces_os_client
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    application = 'application_example' # str | This is a uuid that represents an application
    body = True # bool | Whether or not that application has been onboarded. (optional)

    try:
        # /onboarded [POST]
        api_response = api_instance.onboarded(application, body=body)
        print("The response of ConnectorApi->onboarded:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->onboarded: %s\n" % e)
```



### Parameters {#onboarded-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **str**| This is a uuid that represents an application | 
 **body** | **bool**| Whether or not that application has been onboarded. | [optional] 

### Return type {#onboarded-return-type}

**str**

### Authorization {#onboarded-authorization}

No authorization required

### HTTP request headers {#onboarded-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain


### HTTP response details {#onboarded-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK, This will just return a string of \&quot;OK\&quot;. |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |
**401** | Unauthorized, you will get this in the case that you are trying to ping Pieces_OS but havnt connected yet.\&quot;/connect was not called for your application.\&quot; |  -  |

## **react** {#react}
> str react(application, reaction=reaction)

/\{application\}/reaction [POST]

This will respond to the output generated by the /suggest endpoint.

### Example {#react-example}


```python
import pieces_os_client
from pieces_os_client.models.reaction import Reaction
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    application = 'application_example' # str | 
    reaction = pieces_os_client.Reaction() # Reaction | ** This body will need to be modified. (optional)

    try:
        # /\{application\}/reaction [POST]
        api_response = api_instance.react(application, reaction=reaction)
        print("The response of ConnectorApi->react:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->react: %s\n" % e)
```



### Parameters {#react-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **str**|  | 
 **reaction** | [**Reaction**](../models/Reaction)| ** This body will need to be modified. | [optional] 

### Return type {#react-return-type}

**str**

### Authorization {#react-authorization}

No authorization required

### HTTP request headers {#react-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain


### HTTP response details {#react-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | This string will either (1) be a string of the AssetUid or (2) will be a generic string of &#39;OK&#39; if the asset was not saved and &#39;OK&#39; if the result was just used to send information about the a suggested reuse. |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |
**401** | Unauthorized, you will get this in the case that you are trying to ping Pieces_OS but havnt connected yet.\&quot;/connect was not called for your application.\&quot; |  -  |

## **suggest** {#suggest}
> Suggestion suggest(application, seeded_connector_creation=seeded_connector_creation)

/\{application\}/suggestion [POST]

Invoked whenever a code snippet is copied from an integration. For instance, if a JetBrains user copies code, this endpoint can be called to assess whether to suggest reusing a piece (if reuse is true, the endpoint provides assets that the user may consider using), saving the code snippet, or taking no action.   **Note: This endpoint could potentially accept a SeededFormat for the request body if required.

### Example {#suggest-example}


```python
import pieces_os_client
from pieces_os_client.models.seeded_connector_creation import SeededConnectorCreation
from pieces_os_client.models.suggestion import Suggestion
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    application = 'application_example' # str | 
    seeded_connector_creation = pieces_os_client.SeededConnectorCreation() # SeededConnectorCreation | This is the Snippet that we will compare to all the saved assets to determine what we want to do with it! (optional)

    try:
        # /\{application\}/suggestion [POST]
        api_response = api_instance.suggest(application, seeded_connector_creation=seeded_connector_creation)
        print("The response of ConnectorApi->suggest:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->suggest: %s\n" % e)
```



### Parameters {#suggest-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **str**|  | 
 **seeded_connector_creation** | [**SeededConnectorCreation**](../models/SeededConnectorCreation)| This is the Snippet that we will compare to all the saved assets to determine what we want to do with it! | [optional] 

### Return type {#suggest-return-type}

[**Suggestion**](../models/Suggestion)

### Authorization {#suggest-authorization}

No authorization required

### HTTP request headers {#suggest-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#suggest-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |
**401** | Unauthorized, you will get this in the case that you are trying to ping Pieces_OS but havnt connected yet.\&quot;/connect was not called for your application.\&quot; |  -  |

## **track** {#track}
> str track(application, seeded_connector_tracking=seeded_connector_tracking)

/\{application\}/track [POST]

Abstracts the process of packaging segments on a per-context basis.

### Example {#track-example}


```python
import pieces_os_client
from pieces_os_client.models.seeded_connector_tracking import SeededConnectorTracking
from pieces_os_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:1000
# See configuration.py for a list of all supported configuration parameters.
configuration = pieces_os_client.Configuration(
    host="http://localhost:1000"
)


# Enter a context with an instance of the API client
with pieces_os_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = pieces_os_client.ConnectorApi(api_client)
    application = 'application_example' # str | This is a uuid that represents an application
    seeded_connector_tracking = pieces_os_client.SeededConnectorTracking() # SeededConnectorTracking | The body is able to take in several properties  (optional)

    try:
        # /\{application\}/track [POST]
        api_response = api_instance.track(application, seeded_connector_tracking=seeded_connector_tracking)
        print("The response of ConnectorApi->track:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConnectorApi->track: %s\n" % e)
```



### Parameters {#track-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application** | **str**| This is a uuid that represents an application | 
 **seeded_connector_tracking** | [**SeededConnectorTracking**](../models/SeededConnectorTracking)| The body is able to take in several properties  | [optional] 

### Return type {#track-return-type}

**str**

### Authorization {#track-authorization}

No authorization required

### HTTP request headers {#track-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain


### HTTP response details {#track-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK, This will jsut return a string of \&quot;OK\&quot;. |  -  |
**400** | Bad Request, Application Failed to connect, Please ensure this is a valid integration. This happens in the case a developer provides and incorrect \{application\} (applicationId) within the route that doest match a preregisterd integration. |  -  |
**401** | Unauthorized, you will get this in the case that you are trying to ping Pieces_OS but havnt connected yet.\&quot;/connect was not called for your application.\&quot; |  -  |

