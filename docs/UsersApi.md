# \UsersApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user**](UsersApi.md#add_user) | **POST** /api/v2/users | Create user
[**delete_user_by_id**](UsersApi.md#delete_user_by_id) | **DELETE** /api/v2/users/{id} | Delete user
[**get_authentication_activity**](UsersApi.md#get_authentication_activity) | **GET** /api/v2/users/authentication-activity | Retrieve authentication activity
[**get_latest_authentication_activity_by_user_id**](UsersApi.md#get_latest_authentication_activity_by_user_id) | **GET** /api/v2/users/{id}/authentication-activity/latest | Retrieve latest authentication activity for a user
[**get_users**](UsersApi.md#get_users) | **GET** /api/v2/users | List users
[**update_password_by_user_id**](UsersApi.md#update_password_by_user_id) | **PATCH** /api/v2/users/{id}/password | Update user's password
[**update_user_by_id**](UsersApi.md#update_user_by_id) | **PATCH** /api/v2/users/{id} | Update user



## add_user

> models::UserDto add_user(user_creation_dto)
Create user

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_creation_dto** | [**UserCreationDto**](UserCreationDto.md) |  | [required] |

### Return type

[**models::UserDto**](UserDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_by_id

> delete_user_by_id(id)
Delete user

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_authentication_activity

> models::PageAuthenticationActivityDto get_authentication_activity(unpaged, page, size, sort)
Retrieve authentication activity

Required role: **ADMIN**

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


## get_latest_authentication_activity_by_user_id

> models::AuthenticationActivityDto get_latest_authentication_activity_by_user_id(id, apikey_id)
Retrieve latest authentication activity for a user

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**apikey_id** | Option<**String**> |  |  |

### Return type

[**models::AuthenticationActivityDto**](AuthenticationActivityDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_users

> Vec<models::UserDto> get_users()
List users

Required role: **ADMIN**

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::UserDto>**](UserDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_password_by_user_id

> update_password_by_user_id(id, password_update_dto)
Update user's password

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**password_update_dto** | [**PasswordUpdateDto**](PasswordUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_user_by_id

> update_user_by_id(id, user_update_dto)
Update user

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**user_update_dto** | [**UserUpdateDto**](UserUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

