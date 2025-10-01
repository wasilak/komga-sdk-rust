# \BooksApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**book_analyze**](BooksApi.md#book_analyze) | **POST** /api/v1/books/{bookId}/analyze | Analyze book
[**book_refresh_metadata**](BooksApi.md#book_refresh_metadata) | **POST** /api/v1/books/{bookId}/metadata/refresh | Refresh book metadata
[**delete_book_file**](BooksApi.md#delete_book_file) | **DELETE** /api/v1/books/{bookId}/file | Delete book file
[**delete_book_read_progress**](BooksApi.md#delete_book_read_progress) | **DELETE** /api/v1/books/{bookId}/read-progress | Mark book as unread
[**download_book_file**](BooksApi.md#download_book_file) | **GET** /api/v1/books/{bookId}/file | Download book file
[**download_book_file1**](BooksApi.md#download_book_file1) | **GET** /api/v1/books/{bookId}/file/* | Download book file
[**get_all_books_deprecated**](BooksApi.md#get_all_books_deprecated) | **GET** /api/v1/books | List books
[**get_book_by_id**](BooksApi.md#get_book_by_id) | **GET** /api/v1/books/{bookId} | Get book details
[**get_book_sibling_next**](BooksApi.md#get_book_sibling_next) | **GET** /api/v1/books/{bookId}/next | Get next book in series
[**get_book_sibling_previous**](BooksApi.md#get_book_sibling_previous) | **GET** /api/v1/books/{bookId}/previous | Get previous book in series
[**get_books**](BooksApi.md#get_books) | **POST** /api/v1/books/list | List books
[**get_books_duplicates**](BooksApi.md#get_books_duplicates) | **GET** /api/v1/books/duplicates | List duplicate books
[**get_books_latest**](BooksApi.md#get_books_latest) | **GET** /api/v1/books/latest | List latest books
[**get_books_on_deck**](BooksApi.md#get_books_on_deck) | **GET** /api/v1/books/ondeck | List books on deck
[**get_read_lists_by_book_id**](BooksApi.md#get_read_lists_by_book_id) | **GET** /api/v1/books/{bookId}/readlists | List book's readlists
[**mark_book_read_progress**](BooksApi.md#mark_book_read_progress) | **PATCH** /api/v1/books/{bookId}/read-progress | Mark book's read progress
[**update_book_metadata**](BooksApi.md#update_book_metadata) | **PATCH** /api/v1/books/{bookId}/metadata | Update book metadata
[**update_book_metadata_by_batch**](BooksApi.md#update_book_metadata_by_batch) | **PATCH** /api/v1/books/metadata | Update book metadata in bulk



## book_analyze

> book_analyze(book_id)
Analyze book

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## book_refresh_metadata

> book_refresh_metadata(book_id)
Refresh book metadata

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_book_file

> delete_book_file(book_id)
Delete book file

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_book_read_progress

> delete_book_read_progress(book_id)
Mark book as unread

Mark book as unread

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_book_file

> serde_json::Value download_book_file(book_id)
Download book file

Download the book file.  Required role: **FILE_DOWNLOAD**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/octet-stream, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_book_file1

> serde_json::Value download_book_file1(book_id)
Download book file

Download the book file.  Required role: **FILE_DOWNLOAD**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/octet-stream, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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


## get_book_by_id

> models::BookDto get_book_by_id(book_id)
Get book details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::BookDto**](BookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_sibling_next

> models::BookDto get_book_sibling_next(book_id)
Get next book in series

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::BookDto**](BookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_sibling_previous

> models::BookDto get_book_sibling_previous(book_id)
Get previous book in series

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::BookDto**](BookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_books

> models::PageBookDto get_books(book_search, unpaged, page, size, sort)
List books

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_search** | [**BookSearch**](BookSearch.md) |  | [required] |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_books_duplicates

> models::PageBookDto get_books_duplicates(unpaged, page, size, sort)
List duplicate books

Return books that have the same file hash.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
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


## get_books_latest

> models::PageBookDto get_books_latest(unpaged, page, size)
List latest books

Return newly added or updated books.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_books_on_deck

> models::PageBookDto get_books_on_deck(library_id, page, size)
List books on deck

Return first unread book of series with at least one book read and no books in progress.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_read_lists_by_book_id

> Vec<models::ReadListDto> get_read_lists_by_book_id(book_id)
List book's readlists

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**Vec<models::ReadListDto>**](ReadListDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_book_read_progress

> mark_book_read_progress(book_id, read_progress_update_dto)
Mark book's read progress

Mark book as read and/or change page progress.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**read_progress_update_dto** | [**ReadProgressUpdateDto**](ReadProgressUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_book_metadata

> update_book_metadata(book_id, book_metadata_update_dto)
Update book metadata

Set a field to null to unset the metadata. You can omit fields you don't want to update.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**book_metadata_update_dto** | [**BookMetadataUpdateDto**](BookMetadataUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_book_metadata_by_batch

> update_book_metadata_by_batch(request_body)
Update book metadata in bulk

Set a field to null to unset the metadata. You can omit fields you don't want to update.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, models::BookMetadataUpdateDto>**](BookMetadataUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

