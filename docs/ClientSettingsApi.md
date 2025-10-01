# \ClientSettingsApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_global_settings**](ClientSettingsApi.md#delete_global_settings) | **DELETE** /api/v1/client-settings/global | Delete global settings
[**delete_user_settings**](ClientSettingsApi.md#delete_user_settings) | **DELETE** /api/v1/client-settings/user | Delete user settings
[**get_global_settings**](ClientSettingsApi.md#get_global_settings) | **GET** /api/v1/client-settings/global/list | Retrieve global client settings
[**get_user_settings**](ClientSettingsApi.md#get_user_settings) | **GET** /api/v1/client-settings/user/list | Retrieve user client settings
[**save_global_setting**](ClientSettingsApi.md#save_global_setting) | **PATCH** /api/v1/client-settings/global | Save global settings
[**save_user_setting**](ClientSettingsApi.md#save_user_setting) | **PATCH** /api/v1/client-settings/user | Save user settings



## delete_global_settings

> delete_global_settings(request_body)
Delete global settings

Setting key should be a valid lowercase namespace string like 'application.domain.key'  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**Vec<String>**](String.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_settings

> delete_user_settings(request_body)
Delete user settings

Setting key should be a valid lowercase namespace string like 'application.domain.key'

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**Vec<String>**](String.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_global_settings

> std::collections::HashMap<String, models::ClientSettingDto> get_global_settings()
Retrieve global client settings

For unauthenticated users, only settings with 'allowUnauthorized=true' will be returned.

### Parameters

This endpoint does not need any parameter.

### Return type

[**std::collections::HashMap<String, models::ClientSettingDto>**](ClientSettingDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_user_settings

> std::collections::HashMap<String, models::ClientSettingDto> get_user_settings()
Retrieve user client settings

### Parameters

This endpoint does not need any parameter.

### Return type

[**std::collections::HashMap<String, models::ClientSettingDto>**](ClientSettingDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## save_global_setting

> save_global_setting(request_body)
Save global settings

Setting key should be a valid lowercase namespace string like 'application.domain.key'  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, models::ClientSettingGlobalUpdateDto>**](ClientSettingGlobalUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## save_user_setting

> save_user_setting(request_body)
Save user settings

Setting key should be a valid lowercase namespace string like 'application.domain.key'

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, models::ClientSettingUserUpdateDto>**](ClientSettingUserUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

