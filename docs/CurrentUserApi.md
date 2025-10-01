# \CurrentUserApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_authentication_activity_for_current_user**](CurrentUserApi.md#get_authentication_activity_for_current_user) | **GET** /api/v2/users/me/authentication-activity | Retrieve authentication activity for the current user
[**get_current_user**](CurrentUserApi.md#get_current_user) | **GET** /api/v2/users/me | Retrieve current user
[**update_password_for_current_user**](CurrentUserApi.md#update_password_for_current_user) | **PATCH** /api/v2/users/me/password | Update current user's password



## get_authentication_activity_for_current_user

> models::PageAuthenticationActivityDto get_authentication_activity_for_current_user(unpaged, page, size, sort)
Retrieve authentication activity for the current user

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |[default to 0]
**size** | Option<**i32**> | The size of the page to be returned |  |[default to 20]
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property,(asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PageAuthenticationActivityDto**](PageAuthenticationActivityDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_current_user

> models::UserDto get_current_user(remember_me)
Retrieve current user

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remember_me** | Option<**bool**> |  |  |

### Return type

[**models::UserDto**](UserDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_password_for_current_user

> update_password_for_current_user(password_update_dto)
Update current user's password

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**password_update_dto** | [**PasswordUpdateDto**](PasswordUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

