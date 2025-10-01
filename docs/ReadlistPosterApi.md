# \ReadlistPosterApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_uploaded_read_list_thumbnail**](ReadlistPosterApi.md#add_user_uploaded_read_list_thumbnail) | **POST** /api/v1/readlists/{id}/thumbnails | Add readlist poster
[**delete_user_uploaded_read_list_thumbnail**](ReadlistPosterApi.md#delete_user_uploaded_read_list_thumbnail) | **DELETE** /api/v1/readlists/{id}/thumbnails/{thumbnailId} | Delete readlist poster
[**get_read_list_thumbnail**](ReadlistPosterApi.md#get_read_list_thumbnail) | **GET** /api/v1/readlists/{id}/thumbnail | Get readlist's poster image
[**get_read_list_thumbnail_by_id**](ReadlistPosterApi.md#get_read_list_thumbnail_by_id) | **GET** /api/v1/readlists/{id}/thumbnails/{thumbnailId} | Get readlist poster image
[**get_read_list_thumbnails**](ReadlistPosterApi.md#get_read_list_thumbnails) | **GET** /api/v1/readlists/{id}/thumbnails | List readlist's posters
[**mark_read_list_thumbnail_selected**](ReadlistPosterApi.md#mark_read_list_thumbnail_selected) | **PUT** /api/v1/readlists/{id}/thumbnails/{thumbnailId}/selected | Mark readlist poster as selected



## add_user_uploaded_read_list_thumbnail

> models::ThumbnailReadListDto add_user_uploaded_read_list_thumbnail(id, file, selected)
Add readlist poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**file** | **std::path::PathBuf** |  | [required] |
**selected** | Option<**bool**> |  |  |

### Return type

[**models::ThumbnailReadListDto**](ThumbnailReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_uploaded_read_list_thumbnail

> delete_user_uploaded_read_list_thumbnail(id, thumbnail_id)
Delete readlist poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_list_thumbnail

> std::path::PathBuf get_read_list_thumbnail(id)
Get readlist's poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_list_thumbnail_by_id

> std::path::PathBuf get_read_list_thumbnail_by_id(id, thumbnail_id)
Get readlist poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_list_thumbnails

> Vec<models::ThumbnailReadListDto> get_read_list_thumbnails(id)
List readlist's posters

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**Vec<models::ThumbnailReadListDto>**](ThumbnailReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_read_list_thumbnail_selected

> mark_read_list_thumbnail_selected(id, thumbnail_id)
Mark readlist poster as selected

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

