# \SeriesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_series_file**](SeriesApi.md#delete_series_file) | **DELETE** /api/v1/series/{seriesId}/file | Delete series files
[**download_series_as_zip**](SeriesApi.md#download_series_as_zip) | **GET** /api/v1/series/{seriesId}/file | Download series
[**get_books_by_series_id**](SeriesApi.md#get_books_by_series_id) | **GET** /api/v1/series/{seriesId}/books | List series' books
[**get_collections_by_series_id**](SeriesApi.md#get_collections_by_series_id) | **GET** /api/v1/series/{seriesId}/collections | List series' collections
[**get_series**](SeriesApi.md#get_series) | **POST** /api/v1/series/list | List series
[**get_series_alphabetical_groups**](SeriesApi.md#get_series_alphabetical_groups) | **POST** /api/v1/series/list/alphabetical-groups | List series groups
[**get_series_alphabetical_groups_deprecated**](SeriesApi.md#get_series_alphabetical_groups_deprecated) | **GET** /api/v1/series/alphabetical-groups | List series groups
[**get_series_by_id**](SeriesApi.md#get_series_by_id) | **GET** /api/v1/series/{seriesId} | Get series details
[**get_series_deprecated**](SeriesApi.md#get_series_deprecated) | **GET** /api/v1/series | List series
[**get_series_latest**](SeriesApi.md#get_series_latest) | **GET** /api/v1/series/latest | List latest series
[**get_series_new**](SeriesApi.md#get_series_new) | **GET** /api/v1/series/new | List new series
[**get_series_updated**](SeriesApi.md#get_series_updated) | **GET** /api/v1/series/updated | List updated series
[**mark_series_as_read**](SeriesApi.md#mark_series_as_read) | **POST** /api/v1/series/{seriesId}/read-progress | Mark series as read
[**mark_series_as_unread**](SeriesApi.md#mark_series_as_unread) | **DELETE** /api/v1/series/{seriesId}/read-progress | Mark series as unread
[**series_analyze**](SeriesApi.md#series_analyze) | **POST** /api/v1/series/{seriesId}/analyze | Analyze series
[**series_refresh_metadata**](SeriesApi.md#series_refresh_metadata) | **POST** /api/v1/series/{seriesId}/metadata/refresh | Refresh series metadata
[**update_series_metadata**](SeriesApi.md#update_series_metadata) | **PATCH** /api/v1/series/{seriesId}/metadata | Update series metadata



## delete_series_file

> delete_series_file(series_id)
Delete series files

Delete all of the series' books files on disk.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_series_as_zip

> serde_json::Value download_series_as_zip(series_id)
Download series

Download the whole series as a ZIP file.  Required role: **FILE_DOWNLOAD**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/octet-stream, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_books_by_series_id

> models::PageBookDto get_books_by_series_id(series_id, media_status, read_status, tag, deleted, unpaged, page, size, sort, author)
List series' books

Use POST /api/v1/books/list instead. Deprecated since 1.19.0.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**media_status** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |
**author** | Option<[**Vec<String>**](String.md)> | Author criteria in the format: name,role. Multiple author criteria are supported. |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_collections_by_series_id

> Vec<models::CollectionDto> get_collections_by_series_id(series_id)
List series' collections

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**Vec<models::CollectionDto>**](CollectionDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series

> models::PageSeriesDto get_series(series_search, unpaged, page, size, sort)
List series

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_search** | [**SeriesSearch**](SeriesSearch.md) |  | [required] |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_alphabetical_groups

> Vec<models::GroupCountDto> get_series_alphabetical_groups(series_search)
List series groups

List series grouped by the first character of their sort title.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_search** | [**SeriesSearch**](SeriesSearch.md) |  | [required] |

### Return type

[**Vec<models::GroupCountDto>**](GroupCountDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_alphabetical_groups_deprecated

> Vec<models::GroupCountDto> get_series_alphabetical_groups_deprecated(search, library_id, collection_id, status, read_status, publisher, language, genre, tag, age_rating, release_year, sharing_label, deleted, complete, oneshot, search_regex, author)
List series groups

Use POST /api/v1/series/list/alphabetical-groups instead. Deprecated since 1.19.0.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<[**Vec<String>**](String.md)> |  |  |
**status** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**publisher** | Option<[**Vec<String>**](String.md)> |  |  |
**language** | Option<[**Vec<String>**](String.md)> |  |  |
**genre** | Option<[**Vec<String>**](String.md)> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**age_rating** | Option<[**Vec<String>**](String.md)> |  |  |
**release_year** | Option<[**Vec<String>**](String.md)> |  |  |
**sharing_label** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**complete** | Option<**bool**> |  |  |
**oneshot** | Option<**bool**> |  |  |
**search_regex** | Option<**String**> | Search by regex criteria, in the form: regex,field. Supported fields are TITLE and TITLE_SORT. |  |
**author** | Option<[**Vec<String>**](String.md)> | Author criteria in the format: name,role. Multiple author criteria are supported. |  |

### Return type

[**Vec<models::GroupCountDto>**](GroupCountDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_by_id

> models::SeriesDto get_series_by_id(series_id)
Get series details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**models::SeriesDto**](SeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_deprecated

> models::PageSeriesDto get_series_deprecated(search, library_id, collection_id, status, read_status, publisher, language, genre, tag, age_rating, release_year, sharing_label, deleted, complete, oneshot, unpaged, search_regex, page, size, sort, author)
List series

Use POST /api/v1/series/list instead. Deprecated since 1.19.0.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<[**Vec<String>**](String.md)> |  |  |
**status** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**publisher** | Option<[**Vec<String>**](String.md)> |  |  |
**language** | Option<[**Vec<String>**](String.md)> |  |  |
**genre** | Option<[**Vec<String>**](String.md)> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**age_rating** | Option<[**Vec<String>**](String.md)> |  |  |
**release_year** | Option<[**Vec<String>**](String.md)> |  |  |
**sharing_label** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**complete** | Option<**bool**> |  |  |
**oneshot** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**search_regex** | Option<**String**> | Search by regex criteria, in the form: regex,field. Supported fields are TITLE and TITLE_SORT. |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |
**author** | Option<[**Vec<String>**](String.md)> | Author criteria in the format: name,role. Multiple author criteria are supported. |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_latest

> models::PageSeriesDto get_series_latest(library_id, deleted, oneshot, unpaged, page, size)
List latest series

Return recently added or updated series.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**oneshot** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_new

> models::PageSeriesDto get_series_new(library_id, deleted, oneshot, unpaged, page, size)
List new series

Return newly added series.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**oneshot** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_updated

> models::PageSeriesDto get_series_updated(library_id, deleted, oneshot, unpaged, page, size)
List updated series

Return recently updated series, but not newly added ones.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**oneshot** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageSeriesDto**](PageSeriesDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_series_as_read

> mark_series_as_read(series_id)
Mark series as read

Mark all book for series as read

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_series_as_unread

> mark_series_as_unread(series_id)
Mark series as unread

Mark all book for series as unread

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## series_analyze

> series_analyze(series_id)
Analyze series

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## series_refresh_metadata

> series_refresh_metadata(series_id)
Refresh series metadata

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_series_metadata

> update_series_metadata(series_id, series_metadata_update_dto)
Update series metadata

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**series_metadata_update_dto** | [**SeriesMetadataUpdateDto**](SeriesMetadataUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

