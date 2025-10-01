# \LibrariesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_library**](LibrariesApi.md#add_library) | **POST** /api/v1/libraries | Create a library
[**delete_library_by_id**](LibrariesApi.md#delete_library_by_id) | **DELETE** /api/v1/libraries/{libraryId} | Delete a library
[**get_libraries**](LibrariesApi.md#get_libraries) | **GET** /api/v1/libraries | List all libraries
[**get_library_by_id**](LibrariesApi.md#get_library_by_id) | **GET** /api/v1/libraries/{libraryId} | Get details for a single library
[**library_analyze**](LibrariesApi.md#library_analyze) | **POST** /api/v1/libraries/{libraryId}/analyze | Analyze a library
[**library_empty_trash**](LibrariesApi.md#library_empty_trash) | **POST** /api/v1/libraries/{libraryId}/empty-trash | Empty trash for a library
[**library_refresh_metadata**](LibrariesApi.md#library_refresh_metadata) | **POST** /api/v1/libraries/{libraryId}/metadata/refresh | Refresh metadata for a library
[**library_scan**](LibrariesApi.md#library_scan) | **POST** /api/v1/libraries/{libraryId}/scan | Scan a library
[**update_library_by_id**](LibrariesApi.md#update_library_by_id) | **PATCH** /api/v1/libraries/{libraryId} | Update a library
[**update_library_by_id_deprecated**](LibrariesApi.md#update_library_by_id_deprecated) | **PUT** /api/v1/libraries/{libraryId} | Update a library



## add_library

> models::LibraryDto add_library(library_creation_dto)
Create a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_creation_dto** | [**LibraryCreationDto**](LibraryCreationDto.md) |  | [required] |

### Return type

[**models::LibraryDto**](LibraryDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_library_by_id

> delete_library_by_id(library_id)
Delete a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_libraries

> Vec<models::LibraryDto> get_libraries()
List all libraries

The libraries are filtered based on the current user's permissions

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::LibraryDto>**](LibraryDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_library_by_id

> models::LibraryDto get_library_by_id(library_id)
Get details for a single library

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |

### Return type

[**models::LibraryDto**](LibraryDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## library_analyze

> library_analyze(library_id)
Analyze a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## library_empty_trash

> library_empty_trash(library_id)
Empty trash for a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## library_refresh_metadata

> library_refresh_metadata(library_id)
Refresh metadata for a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## library_scan

> library_scan(library_id, deep)
Scan a library

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |
**deep** | Option<**bool**> |  |  |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_library_by_id

> update_library_by_id(library_id, library_update_dto)
Update a library

You can omit fields you don't want to update  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |
**library_update_dto** | [**LibraryUpdateDto**](LibraryUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_library_by_id_deprecated

> update_library_by_id_deprecated(library_id, library_update_dto)
Update a library

Use PATCH /api/v1/libraries/{libraryId} instead. Deprecated since 1.3.0.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | **String** |  | [required] |
**library_update_dto** | [**LibraryUpdateDto**](LibraryUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

