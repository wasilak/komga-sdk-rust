# \ReadlistsApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_read_list**](ReadlistsApi.md#create_read_list) | **POST** /api/v1/readlists | Create readlist
[**delete_read_list_by_id**](ReadlistsApi.md#delete_read_list_by_id) | **DELETE** /api/v1/readlists/{id} | Delete readlist
[**download_read_list_as_zip**](ReadlistsApi.md#download_read_list_as_zip) | **GET** /api/v1/readlists/{id}/file | Download readlist
[**get_read_list_by_id**](ReadlistsApi.md#get_read_list_by_id) | **GET** /api/v1/readlists/{id} | Get readlist details
[**get_read_lists**](ReadlistsApi.md#get_read_lists) | **GET** /api/v1/readlists | List readlists
[**update_read_list_by_id**](ReadlistsApi.md#update_read_list_by_id) | **PATCH** /api/v1/readlists/{id} | Update readlist



## create_read_list

> models::ReadListDto create_read_list(read_list_creation_dto)
Create readlist

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**read_list_creation_dto** | [**ReadListCreationDto**](ReadListCreationDto.md) |  | [required] |

### Return type

[**models::ReadListDto**](ReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_read_list_by_id

> delete_read_list_by_id(id)
Delete readlist

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


## download_read_list_as_zip

> serde_json::Value download_read_list_as_zip(id)
Download readlist

Download the whole readlist as a ZIP file.  Required role: **FILE_DOWNLOAD**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/octet-stream, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_list_by_id

> models::ReadListDto get_read_list_by_id(id)
Get readlist details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::ReadListDto**](ReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_lists

> models::PageReadListDto get_read_lists(search, library_id, unpaged, page, size)
List readlists

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageReadListDto**](PageReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_read_list_by_id

> update_read_list_by_id(id, read_list_update_dto)
Update readlist

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**read_list_update_dto** | [**ReadListUpdateDto**](ReadListUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

