# \SeriesPosterApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_uploaded_series_thumbnail**](SeriesPosterApi.md#add_user_uploaded_series_thumbnail) | **POST** /api/v1/series/{seriesId}/thumbnails | Add series poster
[**delete_user_uploaded_series_thumbnail**](SeriesPosterApi.md#delete_user_uploaded_series_thumbnail) | **DELETE** /api/v1/series/{seriesId}/thumbnails/{thumbnailId} | Delete series poster
[**get_series_thumbnail**](SeriesPosterApi.md#get_series_thumbnail) | **GET** /api/v1/series/{seriesId}/thumbnail | Get series' poster image
[**get_series_thumbnail_by_id**](SeriesPosterApi.md#get_series_thumbnail_by_id) | **GET** /api/v1/series/{seriesId}/thumbnails/{thumbnailId} | Get series poster image
[**get_series_thumbnails**](SeriesPosterApi.md#get_series_thumbnails) | **GET** /api/v1/series/{seriesId}/thumbnails | List series posters
[**mark_series_thumbnail_selected**](SeriesPosterApi.md#mark_series_thumbnail_selected) | **PUT** /api/v1/series/{seriesId}/thumbnails/{thumbnailId}/selected | Mark series poster as selected



## add_user_uploaded_series_thumbnail

> models::ThumbnailSeriesDto add_user_uploaded_series_thumbnail(series_id, file, selected)
Add series poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**file** | **std::path::PathBuf** |  | [required] |
**selected** | Option<**bool**> |  |  |

### Return type

[**models::ThumbnailSeriesDto**](ThumbnailSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_uploaded_series_thumbnail

> delete_user_uploaded_series_thumbnail(series_id, thumbnail_id)
Delete series poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_thumbnail

> std::path::PathBuf get_series_thumbnail(series_id)
Get series' poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_thumbnail_by_id

> std::path::PathBuf get_series_thumbnail_by_id(series_id, thumbnail_id)
Get series poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_thumbnails

> Vec<models::ThumbnailSeriesDto> get_series_thumbnails(series_id)
List series posters

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**Vec<models::ThumbnailSeriesDto>**](ThumbnailSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_series_thumbnail_selected

> mark_series_thumbnail_selected(series_id, thumbnail_id)
Mark series poster as selected

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

