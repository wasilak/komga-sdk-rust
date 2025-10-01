# \CollectionSeriesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_series_by_collection_id**](CollectionSeriesApi.md#get_series_by_collection_id) | **GET** /api/v1/collections/{id}/series | List collection's series



## get_series_by_collection_id

> models::PageSeriesDto get_series_by_collection_id(id, library_id, status, read_status, publisher, language, genre, tag, age_rating, release_year, deleted, complete, unpaged, page, size, author)
List collection's series

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**status** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**publisher** | Option<[**Vec<String>**](String.md)> |  |  |
**language** | Option<[**Vec<String>**](String.md)> |  |  |
**genre** | Option<[**Vec<String>**](String.md)> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**age_rating** | Option<[**Vec<String>**](String.md)> |  |  |
**release_year** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**complete** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**author** | Option<[**Vec<String>**](String.md)> | Author criteria in the format: name,role. Multiple author criteria are supported. |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

