
# TrackedConversationEventIdentifierDescriptionPairs

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema.md) |  |  [optional]
**conversationCreated** | [**inline**](#ConversationCreated) | The key value pair for an conversation being created. |  [optional]
**conversationReferenced** | [**inline**](#ConversationReferenced) | This means that an conversation was view/used while the user was looking at the default view. |  [optional]
**conversationDeleted** | [**inline**](#ConversationDeleted) | A conversation was deleted |  [optional]
**conversationSummaryAnnotationGeneratedByTheUser** | [**inline**](#ConversationSummaryAnnotationGeneratedByTheUser) | A conversation summary was generated by the user |  [optional]
**conversationNameUpdatedByTheSystem** | [**inline**](#ConversationNameUpdatedByTheSystem) | A conversation was renamed by the system |  [optional]
**conversationNameUpdatedByTheUser** | [**inline**](#ConversationNameUpdatedByTheUser) | A conversation was renamed by the user |  [optional]
**conversationSummaryAnnotationGeneratedByTheSystem** | [**inline**](#ConversationSummaryAnnotationGeneratedByTheSystem) | A conversation summary was generated |  [optional]


<a id="ConversationCreated"></a>
## Enum: conversation_created
Name | Value
---- | -----
conversationCreated | a_conversation_was_created


<a id="ConversationReferenced"></a>
## Enum: conversation_referenced
Name | Value
---- | -----
conversationReferenced | a_conversation_was_referenced_by_the_user


<a id="ConversationDeleted"></a>
## Enum: conversation_deleted
Name | Value
---- | -----
conversationDeleted | a_conversation_was_deleted


<a id="ConversationSummaryAnnotationGeneratedByTheUser"></a>
## Enum: conversation_summary_annotation_generated_by_the_user
Name | Value
---- | -----
conversationSummaryAnnotationGeneratedByTheUser | a_conversation_summary_annotation_was_generated_by_the_user


<a id="ConversationNameUpdatedByTheSystem"></a>
## Enum: conversation_name_updated_by_the_system
Name | Value
---- | -----
conversationNameUpdatedByTheSystem | a_conversation_was_renamed_by_the_system


<a id="ConversationNameUpdatedByTheUser"></a>
## Enum: conversation_name_updated_by_the_user
Name | Value
---- | -----
conversationNameUpdatedByTheUser | a_conversation_was_renamed_by_the_user


<a id="ConversationSummaryAnnotationGeneratedByTheSystem"></a>
## Enum: conversation_summary_annotation_generated_by_the_system
Name | Value
---- | -----
conversationSummaryAnnotationGeneratedByTheSystem | a_conversation_summary_annotation_was_generated_by_the_system


