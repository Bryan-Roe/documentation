---
title: Users API | TypeScript SDK
---

# Users API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**authenticateFromOauthToken**](UsersApi#authenticatefromoauthtoken) | **POST** /users/authenticate/from_token | /users/authenticate/from_token [POST]
[**usersDisconnectUser**](UsersApi#usersdisconnectuser) | **POST** /users/\{user\}/disconnect | /users/\{user\}/disconnect [POST]
[**usersSnapshot**](UsersApi#userssnapshot) | **GET** /users | /users [GET]
[**usersSpecificUserSnapshot**](UsersApi#usersspecificusersnapshot) | **GET** /users/\{user\} | /users/\{user\} [GET] Scoped to Users


## **authenticateFromOauthToken** {#authenticatefromoauthtoken}
> UserProfile authenticateFromOauthToken()

Creates a User From a oAuth Token

### Example {#authenticatefromoauthtoken-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.UsersApi(configuration)

const body: Pieces.AuthenticateFromOauthTokenRequest = {
// OAuthToken |  (optional)
oAuthToken: ,
};

apiInstance.authenticateFromOauthToken(body).then((data: UserProfile) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#authenticatefromoauthtoken-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **oAuthToken** | **OAuthToken**|  |


### Return type {#authenticatefromoauthtoken-return-type}

[**UserProfile**](../models/UserProfile)

### HTTP request headers {#authenticatefromoauthtoken-http-request-headers}

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details {#authenticatefromoauthtoken-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |

## **usersDisconnectUser** {#usersdisconnectuser}
> Users usersDisconnectUser()

Locally Removing a user for the purpose of Signing Out

### Example {#usersdisconnectuser-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.UsersApi(configuration)

const body: Pieces.UsersDisconnectUserRequest = {
// string
user: user_example,
};

apiInstance.usersDisconnectUser(body).then((data: Users) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#usersdisconnectuser-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user** | [**string**] |  | defaults to undefined


### Return type {#usersdisconnectuser-return-type}

[**Users**](../models/Users)

### HTTP request headers {#usersdisconnectuser-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details {#usersdisconnectuser-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |

## **usersSnapshot** {#userssnapshot}
> Users usersSnapshot()

this will return a snapshot of all of the users that are in the users database. TODO might want to make this internal.

### Example {#userssnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.UsersApi(configuration)

apiInstance.usersSnapshot().then((data: Users) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#userssnapshot-parameters}

This endpoint does not need any parameters.


### Return type {#userssnapshot-return-type}

[**Users**](../models/Users)

### HTTP request headers {#userssnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details {#userssnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |

## **usersSpecificUserSnapshot** {#usersspecificusersnapshot}
> UserProfile usersSpecificUserSnapshot()

This enables the client to get the current user.  This endpoint will return a UserPRofile or will throw an error since you are sending user uid.

### Example {#usersspecificusersnapshot-example}

```typescript
import * as Pieces from '@pieces.app/pieces-os-client'

const configuration = Pieces.Configuration()
const apiInstance = new Pieces.UsersApi(configuration)

const body: Pieces.UsersSpecificUserSnapshotRequest = {
// string | The id (uuid) for a specific user.
user: 497f6eca-6276-4993-bfeb-53cbbbba6f08,
};

apiInstance.usersSpecificUserSnapshot(body).then((data: UserProfile) => {
console.log('API called successfully. Returned data: ' + data)
}).catch((error: unknown) => console.error(error))
```

### Parameters {#usersspecificusersnapshot-parameters}


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user** | [**string**] | The id (uuid) for a specific user. | defaults to undefined


### Return type {#usersspecificusersnapshot-return-type}

[**UserProfile**](../models/UserProfile)

### HTTP request headers {#usersspecificusersnapshot-http-request-headers}

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details {#usersspecificusersnapshot-http-response-details}
| Status code | Description | Response headers
|-------------|-------------|------------------
**200** | OK |  -  |


