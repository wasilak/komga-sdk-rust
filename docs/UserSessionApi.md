# \UserSessionApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convert_header_session_to_cookie**](UserSessionApi.md#convert_header_session_to_cookie) | **GET** /api/v1/login/set-cookie | Set cookie
[**post_logout**](UserSessionApi.md#post_logout) | **GET** /api/logout | Logout
[**post_logout1**](UserSessionApi.md#post_logout1) | **POST** /api/logout | Logout



## convert_header_session_to_cookie

> convert_header_session_to_cookie()
Set cookie

Forcefully return Set-Cookie header, even if the session is contained in the X-Auth-Token header.

### Parameters

This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_logout

> post_logout()
Logout

Invalidates the current session and clean up any remember-me authentication.

### Parameters

This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_logout1

> post_logout1()
Logout

Invalidates the current session and clean up any remember-me authentication.

### Parameters

This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

