---
title: OpenAI API | Python SDK
---

# OpenAI API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**open_ai_models_list**](OpenAIApi#open_ai_models_list) | **POST** /open_ai/models/list | /open_ai/models/list [POST]


## **open_ai_models_list** {#open_ai_models_list}
> OpenAIModelsListOutput open_ai_models_list(open_ai_models_list_input=open_ai_models_list_input)

/open_ai/models/list [POST]

This will get a list of all of your Models from OpenAI w/ you user.auth0.openAI.apiKey.  if the user is unauthenticated or if the openAI key doesnt exist or if it is invalid we will return a 401.  Requires internet as this will ping out to OpenAI's server to get the models.

### Example {#open_ai_models_list-example}


```python
import pieces_os_client
from pieces_os_client.models.open_ai_models_list_input import OpenAIModelsListInput
from pieces_os_client.models.open_ai_models_list_output import OpenAIModelsListOutput
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
    api_instance = OpenAI API(api_client)
    open_ai_models_list_input = pieces_os_client.OpenAIModelsListInput() # OpenAIModelsListInput |  (optional)

    try:
        # /open_ai/models/list [POST]
        api_response = api_instance.open_ai_models_list(open_ai_models_list_input=open_ai_models_list_input)
        print("The response of OpenAIApi->open_ai_models_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OpenAIApi->open_ai_models_list: %s\n" % e)
```



### Parameters {#open_ai_models_list-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **open_ai_models_list_input** | [**OpenAIModelsListInput**](../models/OpenAIModelsListInput)|  | [optional] 

### Return type {#open_ai_models_list-return-type}

[**OpenAIModelsListOutput**](../models/OpenAIModelsListOutput)

### Authorization {#open_ai_models_list-authorization}

No authorization required

### HTTP request headers {#open_ai_models_list-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain


### HTTP response details {#open_ai_models_list-http-response-details}

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Invalid Authentication, Incorrect API key provided or organization |  -  |
**500** | Internal Server Error |  -  |

