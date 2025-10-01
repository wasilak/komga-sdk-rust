# \ApiKeysApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_api_key_for_current_user**](ApiKeysApi.md#create_api_key_for_current_user) | **POST** /api/v2/users/me/api-keys | Create API key
[**delete_api_key_by_key_id**](ApiKeysApi.md#delete_api_key_by_key_id) | **DELETE** /api/v2/users/me/api-keys/{keyId} | Delete API key
[**get_api_keys_for_current_user**](ApiKeysApi.md#get_api_keys_for_current_user) | **GET** /api/v2/users/me/api-keys | Retrieve API keys



## create_api_key_for_current_user

> models::ApiKeyDto create_api_key_for_current_user(api_key_request_dto)
Create API key

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**api_key_request_dto** | [**ApiKeyRequestDto**](ApiKeyRequestDto.md) |  | [required] |

### Return type

[**models::ApiKeyDto**](ApiKeyDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_api_key_by_key_id

> delete_api_key_by_key_id(key_id)
Delete API key

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**key_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_api_keys_for_current_user

> Vec<models::ApiKeyDto> get_api_keys_for_current_user()
Retrieve API keys

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::ApiKeyDto>**](ApiKeyDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

