---
title: OS API | Dart SDK
---

# OS API

All URIs are relative to `http://localhost:1000`

Method | HTTP request | Description
------------- | ------------- | -------------
[**linkProvider**](OSApi#linkprovider) | **POST** /os/link_provider | /os/link_provider [POST]
[**osDeviceInformation**](OSApi#osdeviceinformation) | **GET** /os/device/information | /os/device/information [GET]
[**osPermissions**](OSApi#ospermissions) | **GET** /os/permissions | /os/permissions [GET]
[**osPermissionsRequest**](OSApi#ospermissionsrequest) | **POST** /os/permissions/request | /os/permissions/request [POST]
[**osRestart**](OSApi#osrestart) | **GET** /os/restart | Your GET endpoint
[**osUpdateCheck**](OSApi#osupdatecheck) | **POST** /os/update/check | /os/update/check [POST]
[**pickFiles**](OSApi#pickfiles) | **POST** /os/files/pick | /os/files/pick [POST]
[**pickFolders**](OSApi#pickfolders) | **POST** /os/folders/pick | /os/folders/pick [POST]
[**signIntoOS**](OSApi#signintoos) | **POST** /os/sign_in | 
[**signOutOfOS**](OSApi#signoutofos) | **POST** /os/sign_out | /os/sign_out [POST]


## **linkProvider** {#linkprovider}
> ReturnedUserProfile linkProvider(seededExternalProvider)

/os/link_provider [POST]

This will link an external provider to your current auth0 account.  Will throw errors if your user is not signed in.

### Example {#linkprovider-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();
final seededExternalProvider = SeededExternalProvider(); // SeededExternalProvider | 

try {
    final result = api_instance.linkProvider(seededExternalProvider);
    print(result);
} catch (e) {
    print('Exception when calling OSApi->linkProvider: $e\n');
}
```

### Parameters {#linkprovider-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **seededExternalProvider** | [**SeededExternalProvider**](../models/SeededExternalProvider) |  | [optional] 

### Return type {#linkprovider-return-type}

[**ReturnedUserProfile**](../models/ReturnedUserProfile)

### Authorization {#linkprovider-authorization}

No authorization required

### HTTP request headers {#linkprovider-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **osDeviceInformation** {#osdeviceinformation}
> OSDeviceInformationReturnable osDeviceInformation()

/os/device/information [GET]

This will get information related to your specific device.

### Example {#osdeviceinformation-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    final result = api_instance.osDeviceInformation();
    print(result);
} catch (e) {
    print('Exception when calling OSApi->osDeviceInformation: $e\n');
}
```

### Parameters {#osdeviceinformation-parameters}
This endpoint does not need any parameter.

### Return type {#osdeviceinformation-return-type}

[**OSDeviceInformationReturnable**](../models/OSDeviceInformationReturnable)

### Authorization {#osdeviceinformation-authorization}

No authorization required

### HTTP request headers {#osdeviceinformation-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

## **osPermissions** {#ospermissions}
> OSPermissions osPermissions()

/os/permissions [GET]

This will only work on Macos and Windows.  And will get the permissions of the user's local machine w/ regard to anything needed to effectively run PiecesOS.  Note: this will let us know if we need to tell them to take action to enable any given permissions

### Example {#ospermissions-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    final result = api_instance.osPermissions();
    print(result);
} catch (e) {
    print('Exception when calling OSApi->osPermissions: $e\n');
}
```

### Parameters {#ospermissions-parameters}
This endpoint does not need any parameter.

### Return type {#ospermissions-return-type}

[**OSPermissions**](../models/OSPermissions)

### Authorization {#ospermissions-authorization}

No authorization required

### HTTP request headers {#ospermissions-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

## **osPermissionsRequest** {#ospermissionsrequest}
> OSPermissions osPermissionsRequest(oSPermissions)

/os/permissions/request [POST]

This will only work on Macos and Windows.  This will request permissions for the given inputs

### Example {#ospermissionsrequest-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();
final oSPermissions = OSPermissions(); // OSPermissions | 

try {
    final result = api_instance.osPermissionsRequest(oSPermissions);
    print(result);
} catch (e) {
    print('Exception when calling OSApi->osPermissionsRequest: $e\n');
}
```

### Parameters {#ospermissionsrequest-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **oSPermissions** | [**OSPermissions**](../models/OSPermissions) |  | [optional] 

### Return type {#ospermissionsrequest-return-type}

[**OSPermissions**](../models/OSPermissions)

### Authorization {#ospermissionsrequest-authorization}

No authorization required

### HTTP request headers {#ospermissionsrequest-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **osRestart** {#osrestart}
> osRestart()

Your GET endpoint

This will restart PiecesOS, if successfull with return a 204. This is a LOCALOS Only Endpoint.

### Example {#osrestart-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    api_instance.osRestart();
} catch (e) {
    print('Exception when calling OSApi->osRestart: $e\n');
}
```

### Parameters {#osrestart-parameters}
This endpoint does not need any parameter.

### Return type {#osrestart-return-type}

void (empty response body)

### Authorization {#osrestart-authorization}

No authorization required

### HTTP request headers {#osrestart-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: text/plain

## **osUpdateCheck** {#osupdatecheck}
> CheckedOSUpdate osUpdateCheck(uncheckedOSUpdate)

/os/update/check [POST]

This is a helper endpoint that will check the status of an update for PiecesOS. IE if there is an update downloading, if there is one available, but the downloading has not started... etc

### Example {#osupdatecheck-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();
final uncheckedOSUpdate = UncheckedOSUpdate(); // UncheckedOSUpdate | 

try {
    final result = api_instance.osUpdateCheck(uncheckedOSUpdate);
    print(result);
} catch (e) {
    print('Exception when calling OSApi->osUpdateCheck: $e\n');
}
```

### Parameters {#osupdatecheck-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uncheckedOSUpdate** | [**UncheckedOSUpdate**](../models/UncheckedOSUpdate) |  | [optional] 

### Return type {#osupdatecheck-return-type}

[**CheckedOSUpdate**](../models/CheckedOSUpdate)

### Authorization {#osupdatecheck-authorization}

No authorization required

### HTTP request headers {#osupdatecheck-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **pickFiles** {#pickfiles}
> List\<String\>** pickFiles(filePickerInput)

/os/files/pick [POST]

This will trigger a filer picker and return the string paths of the files that were selected.

### Example {#pickfiles-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();
final filePickerInput = FilePickerInput(); // FilePickerInput | 

try {
    final result = api_instance.pickFiles(filePickerInput);
    print(result);
} catch (e) {
    print('Exception when calling OSApi->pickFiles: $e\n');
}
```

### Parameters {#pickfiles-parameters}

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filePickerInput** | [**FilePickerInput**](../models/FilePickerInput) |  | [optional] 

### Return type {#pickfiles-return-type}

**List\<String\>**

### Authorization {#pickfiles-authorization}

No authorization required

### HTTP request headers {#pickfiles-http-request-headers}

 - **Content-Type**: application/json
 - **Accept**: application/json, text/plain

## **pickFolders** {#pickfolders}
> List\<String\>** pickFolders()

/os/folders/pick [POST]

This will trigger a folder picker and return the string paths of the folders that were selected.

### Example {#pickfolders-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    final result = api_instance.pickFolders();
    print(result);
} catch (e) {
    print('Exception when calling OSApi->pickFolders: $e\n');
}
```

### Parameters {#pickfolders-parameters}
This endpoint does not need any parameter.

### Return type {#pickfolders-return-type}

**List\<String\>**

### Authorization {#pickfolders-authorization}

No authorization required

### HTTP request headers {#pickfolders-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json, text/plain

## **signIntoOS** {#signintoos}
> UserProfile signIntoOS()



A trigger that launches a Sign into OS Server

### Example {#signintoos-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    final result = api_instance.signIntoOS();
    print(result);
} catch (e) {
    print('Exception when calling OSApi->signIntoOS: $e\n');
}
```

### Parameters {#signintoos-parameters}
This endpoint does not need any parameter.

### Return type {#signintoos-return-type}

[**UserProfile**](../models/UserProfile)

### Authorization {#signintoos-authorization}

No authorization required

### HTTP request headers {#signintoos-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

## **signOutOfOS** {#signoutofos}
> Users signOutOfOS()

/os/sign_out [POST]

A trigger that signs out a user from the OS

### Example {#signoutofos-example}
```dart
import 'package:core_openapi/api.dart';

final api_instance = OSApi();

try {
    final result = api_instance.signOutOfOS();
    print(result);
} catch (e) {
    print('Exception when calling OSApi->signOutOfOS: $e\n');
}
```

### Parameters {#signoutofos-parameters}
This endpoint does not need any parameter.

### Return type {#signoutofos-return-type}

[**Users**](../models/Users)

### Authorization {#signoutofos-authorization}

No authorization required

### HTTP request headers {#signoutofos-http-request-headers}

 - **Content-Type**: Not defined
 - **Accept**: application/json

