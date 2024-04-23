---
title: ExternalProvider | Python SDK
---

# ExternalProvider

I know that profileData and user_id have differeing casing but they are done because they map to Auth0's projeecties.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_schema** | [**EmbeddedModelSchema**](EmbeddedModelSchema) |  | [optional] 
**type** | [**ExternalProviderTypeEnum**](ExternalProviderTypeEnum) |  | 
**user_id** | **str** | This is the user_id within the provider. | 
**access_token** | **str** | This is optional here, but will be present for BB, Github, and google. | [optional] 
**expires_in** | **int** | Some providers have an expiration on their access token. IE BB, Google, NOT Github. | [optional] 
**created** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**updated** | [**GroupedTimestamp**](GroupedTimestamp) |  | 
**profile_data** | [**ExternalProviderProfileData**](ExternalProviderProfileData) |  | [optional] 
**connection** | **str** | This is an optional field that will be provided onentreprise connections. ie is type &#x3D;&#x3D; waad then connection might be PiecesApp. However is other cases,you my find your provider and connection is the exact same string. To decifer between the two, you can use the isSocial bool. | [optional] 
**is_social** | **bool** |  | [optional] 


