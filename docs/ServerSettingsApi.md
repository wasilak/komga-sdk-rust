# \ServerSettingsApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_server_settings**](ServerSettingsApi.md#get_server_settings) | **GET** /api/v1/settings | Retrieve server settings
[**update_server_settings**](ServerSettingsApi.md#update_server_settings) | **PATCH** /api/v1/settings | Update server settings



## get_server_settings

> models::SettingsDto get_server_settings()
Retrieve server settings

Required role: **ADMIN**

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::SettingsDto**](SettingsDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_server_settings

> update_server_settings(settings_update_dto)
Update server settings

You can omit fields you don't want to update  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**settings_update_dto** | [**SettingsUpdateDto**](SettingsUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

