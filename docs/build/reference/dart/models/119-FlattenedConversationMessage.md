---
title: FlattenedConversationMessage | Dart SDK
---

# FlattenedConversationMessage

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**id** | **String** |  | 
**created** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**updated** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**deleted** | [**GroupedTimestamp**](GroupedTimestamp) |  | [optional] 
**model** | [**Model**](Model) |  | [optional] 
**fragment** | [**FragmentFormat**](FragmentFormat) |  | [optional] 
**conversation** | [**ReferencedConversation**](ReferencedConversation) |  | 
**sentiment** | [**ConversationMessageSentimentEnum**](ConversationMessageSentimentEnum) |  | [optional] 
**role** | [**QGPTConversationMessageRoleEnum**](QGPTConversationMessageRoleEnum) |  | 
**score** | [**Score**](Score) |  | [optional] 
**annotations** | [**FlattenedAnnotations**](FlattenedAnnotations) |  | [optional] 


