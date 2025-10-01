# \DeprecatedApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_all_books_deprecated**](DeprecatedApi.md#get_all_books_deprecated) | **GET** /api/v1/books | List books
[**get_authors_deprecated**](DeprecatedApi.md#get_authors_deprecated) | **GET** /api/v1/authors | List authors
[**get_books_by_series_id**](DeprecatedApi.md#get_books_by_series_id) | **GET** /api/v1/series/{seriesId}/books | List series' books
[**get_series_alphabetical_groups_deprecated**](DeprecatedApi.md#get_series_alphabetical_groups_deprecated) | **GET** /api/v1/series/alphabetical-groups | List series groups
[**get_series_deprecated**](DeprecatedApi.md#get_series_deprecated) | **GET** /api/v1/series | List series
[**update_library_by_id_deprecated**](DeprecatedApi.md#update_library_by_id_deprecated) | **PUT** /api/v1/libraries/{libraryId} | Update a library



## get_all_books_deprecated

> models::PageBookDto get_all_books_deprecated(search, library_id, media_status, read_status, released_after, tag, unpaged, page, size, sort)
List books

Use POST /api/v1/books/list instead. Deprecated since 1.19.0.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**media_status** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**released_after** | Option<**String**> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_authors_deprecated

> Vec<models::AuthorDto> get_authors_deprecated(search, library_id, collection_id, series_id)
List authors

Use GET /api/v2/authors instead. Deprecated since 1.20.0.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |[default to ]
**library_id** | Option<**String**> |  |  |
**collection_id** | Option<**String**> |  |  |
**series_id** | Option<**String**> |  |  |

### Return type

[**Vec<models::AuthorDto>**](AuthorDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

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

