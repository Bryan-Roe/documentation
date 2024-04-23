---
title: QGPTRepromptInput | Python SDK
---

# QGPTRepromptInput

Query is your followup question.  Conversation is a list of the back and fourth with the qgpt bot. where the first entry in the array was the last message sent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**query** | **str** |  | 
**conversation** | [**QGPTConversation**](QGPTConversation) |  | 
**application** | **str** | optional application id | [optional] 
**model** | **str** | optional model id | [optional] 
**pipeline** | [**QGPTPromptPipeline**](QGPTPromptPipeline) |  | [optional] 


