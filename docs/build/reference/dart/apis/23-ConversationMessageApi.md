---
title: ConversationMessage API | Dart SDK
---

# ConversationMessage API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**messageAssociateAnnotation**](ConversationMessageApi#messageassociateannotation) | **POST** /message/\{message\}/annotations/associate/\{annotation\} | /message/\{message\}/annotations/associate/\{annotation\} [POST]
[**messageDisassociateAnnotation**](ConversationMessageApi#messagedisassociateannotation) | **POST** /message/\{message\}/annotations/disassociate/\{annotation\} | /message/\{message\}/annotations/disassociate/\{annotation\} [POST]
[**messageScoresIncrement**](ConversationMessageApi#messagescoresincrement) | **POST** /message/\{message\}/scores/increment | '/message/\{message\}/scores/increment' [POST]
[**messageSpecificMessageSnapshot**](ConversationMessageApi#messagespecificmessagesnapshot) | **GET** /message/\{message\} | /message/\{message\} [GET]
[**messageSpecificMessageUpdate**](ConversationMessageApi#messagespecificmessageupdate) | **POST** /message/update | /message/update [GET]
[**messageUpdateValue**](ConversationMessageApi#messageupdatevalue) | **POST** /message/update/value | /message/update/value [POST]


## **messageAssociateAnnotation** {#messageassociateannotation}
> messageAssociateAnnotation(annotation, message)

/message/\{message\}/annotations/associate/\{annotation\} [POST]

This will associate a message with an annotation.

### Example {#messageassociateannotation-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final annotation = annotation_example; // String | This is a specific annotation uuid.
final message = message_example; // String | This is the uuid of a message.

try {
    api_instance.messageAssociateAnnotation(annotation, message);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageAssociateAnnotation: $e\n');
}
```

### Parameters {#messageassociateannotation-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation** | **String** | This is a specific annotation uuid. | 
 **message** | **String** | This is the uuid of a message. | 

### Return type {#messageassociateannotation-return-type}

void (empty response body)

### Authorization {#messageassociateannotation-authorization}

No authorization required

### HTTP request headers {#messageassociateannotation-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **messageDisassociateAnnotation** {#messagedisassociateannotation}
> messageDisassociateAnnotation(annotation, message)

/message/\{message\}/annotations/disassociate/\{annotation\} [POST]

This will enable us to dissassociate a message from an annotation.

### Example {#messagedisassociateannotation-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final annotation = annotation_example; // String | This is a specific annotation uuid.
final message = message_example; // String | This is the uuid of a message.

try {
    api_instance.messageDisassociateAnnotation(annotation, message);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageDisassociateAnnotation: $e\n');
}
```

### Parameters {#messagedisassociateannotation-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **annotation** | **String** | This is a specific annotation uuid. | 
 **message** | **String** | This is the uuid of a message. | 

### Return type {#messagedisassociateannotation-return-type}

void (empty response body)

### Authorization {#messagedisassociateannotation-authorization}

No authorization required

### HTTP request headers {#messagedisassociateannotation-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **messageScoresIncrement** {#messagescoresincrement}
> messageScoresIncrement(message, seededScoreIncrement)

'/message/\{message\}/scores/increment' [POST]

This will take in a SeededScoreIncrement and will increment the material relative to the incoming body.

### Example {#messagescoresincrement-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final message = message_example; // String | This is the uuid of a message.
final seededScoreIncrement = SeededScoreIncrement(); // SeededScoreIncrement | 

try {
    api_instance.messageScoresIncrement(message, seededScoreIncrement);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageScoresIncrement: $e\n');
}
```

### Parameters {#messagescoresincrement-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **String** | This is the uuid of a message. | 
 **seededScoreIncrement** | [**SeededScoreIncrement**](../models/SeededScoreIncrement) |  | [optional] 

### Return type {#messagescoresincrement-return-type}

void (empty response body)

### Authorization {#messagescoresincrement-authorization}

No authorization required

### HTTP request headers {#messagescoresincrement-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: text/plain

## **messageSpecificMessageSnapshot** {#messagespecificmessagesnapshot}
> ConversationMessage messageSpecificMessageSnapshot(message, transferables)

/message/\{message\} [GET]

This will get a specific snapshot of a message

### Example {#messagespecificmessagesnapshot-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final message = message_example; // String | This is the uuid of a message.
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)

try {
    final result = api_instance.messageSpecificMessageSnapshot(message, transferables);
    print(result);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageSpecificMessageSnapshot: $e\n');
}
```

### Parameters {#messagespecificmessagesnapshot-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **String** | This is the uuid of a message. | 
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 

### Return type {#messagespecificmessagesnapshot-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#messagespecificmessagesnapshot-authorization}

No authorization required

### HTTP request headers {#messagespecificmessagesnapshot-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

## **messageSpecificMessageUpdate** {#messagespecificmessageupdate}
> ConversationMessage messageSpecificMessageUpdate(transferables, conversationMessage)

/message/update [GET]

This will update a conversation message.

### Example {#messagespecificmessageupdate-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
final conversationMessage = ConversationMessage(); // ConversationMessage | 

try {
    final result = api_instance.messageSpecificMessageUpdate(transferables, conversationMessage);
    print(result);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageSpecificMessageUpdate: $e\n');
}
```

### Parameters {#messagespecificmessageupdate-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **conversationMessage** | [**ConversationMessage**](../models/ConversationMessage) |  | [optional] 

### Return type {#messagespecificmessageupdate-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#messagespecificmessageupdate-authorization}

No authorization required

### HTTP request headers {#messagespecificmessageupdate-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **messageUpdateValue** {#messageupdatevalue}
> ConversationMessage messageUpdateValue(transferables, conversationMessage)

/message/update/value [POST]

This will update the value of a conversation message.

### Example {#messageupdatevalue-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = ConversationMessageApi();
final transferables = true; // bool | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement)
final conversationMessage = ConversationMessage(); // ConversationMessage | 

try {
    final result = api_instance.messageUpdateValue(transferables, conversationMessage);
    print(result);
} catch (e) {
    print('Exception when calling ConversationMessageApi->messageUpdateValue: $e\n');
}
```

### Parameters {#messageupdatevalue-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transferables** | **bool** | This is a boolean that will decided if we are want to return the transferable data (default) or not(performance enhancement) | [optional] 
 **conversationMessage** | [**ConversationMessage**](../models/ConversationMessage) |  | [optional] 

### Return type {#messageupdatevalue-return-type}

[**ConversationMessage**](../models/ConversationMessage)

### Authorization {#messageupdatevalue-authorization}

No authorization required

### HTTP request headers {#messageupdatevalue-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

