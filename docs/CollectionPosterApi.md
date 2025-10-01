# \CollectionPosterApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_uploaded_collection_thumbnail**](CollectionPosterApi.md#add_user_uploaded_collection_thumbnail) | **POST** /api/v1/collections/{id}/thumbnails | Add collection poster
[**delete_user_uploaded_collection_thumbnail**](CollectionPosterApi.md#delete_user_uploaded_collection_thumbnail) | **DELETE** /api/v1/collections/{id}/thumbnails/{thumbnailId} | Delete collection poster
[**get_collection_thumbnail**](CollectionPosterApi.md#get_collection_thumbnail) | **GET** /api/v1/collections/{id}/thumbnail | Get collection's poster image
[**get_collection_thumbnail_by_id**](CollectionPosterApi.md#get_collection_thumbnail_by_id) | **GET** /api/v1/collections/{id}/thumbnails/{thumbnailId} | Get collection poster image
[**get_collection_thumbnails**](CollectionPosterApi.md#get_collection_thumbnails) | **GET** /api/v1/collections/{id}/thumbnails | List collection's posters
[**mark_collection_thumbnail_selected**](CollectionPosterApi.md#mark_collection_thumbnail_selected) | **PUT** /api/v1/collections/{id}/thumbnails/{thumbnailId}/selected | Mark collection poster as selected



## add_user_uploaded_collection_thumbnail

> models::ThumbnailSeriesCollectionDto add_user_uploaded_collection_thumbnail(id, file, selected)
Add collection poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**file** | **std::path::PathBuf** |  | [required] |
**selected** | Option<**bool**> |  |  |

### Return type

[**models::ThumbnailSeriesCollectionDto**](ThumbnailSeriesCollectionDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_uploaded_collection_thumbnail

> delete_user_uploaded_collection_thumbnail(id, thumbnail_id)
Delete collection poster

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


## get_collection_thumbnail

> std::path::PathBuf get_collection_thumbnail(id)
Get collection's poster image

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


## get_collection_thumbnail_by_id

> std::path::PathBuf get_collection_thumbnail_by_id(id, thumbnail_id)
Get collection poster image

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


## get_collection_thumbnails

> Vec<models::ThumbnailSeriesCollectionDto> get_collection_thumbnails(id)
List collection's posters

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**Vec<models::ThumbnailSeriesCollectionDto>**](ThumbnailSeriesCollectionDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_collection_thumbnail_selected

> mark_collection_thumbnail_selected(id, thumbnail_id)
Mark collection poster as selected

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

