# \ReadlistBooksApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_book_sibling_next_in_read_list**](ReadlistBooksApi.md#get_book_sibling_next_in_read_list) | **GET** /api/v1/readlists/{id}/books/{bookId}/next | Get next book in readlist
[**get_book_sibling_previous_in_read_list**](ReadlistBooksApi.md#get_book_sibling_previous_in_read_list) | **GET** /api/v1/readlists/{id}/books/{bookId}/previous | Get previous book in readlist
[**get_books_by_read_list_id**](ReadlistBooksApi.md#get_books_by_read_list_id) | **GET** /api/v1/readlists/{id}/books | List readlist's books



## get_book_sibling_next_in_read_list

> models::BookDto get_book_sibling_next_in_read_list(id, book_id)
Get next book in readlist

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**book_id** | **String** |  | [required] |

### Return type

[**models::BookDto**](BookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_sibling_previous_in_read_list

> models::BookDto get_book_sibling_previous_in_read_list(id, book_id)
Get previous book in readlist

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**book_id** | **String** |  | [required] |

### Return type

[**models::BookDto**](BookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_books_by_read_list_id

> models::PageBookDto get_books_by_read_list_id(id, library_id, read_status, tag, media_status, deleted, unpaged, page, size, author)
List readlist's books

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**read_status** | Option<[**Vec<String>**](String.md)> |  |  |
**tag** | Option<[**Vec<String>**](String.md)> |  |  |
**media_status** | Option<[**Vec<String>**](String.md)> |  |  |
**deleted** | Option<**bool**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**author** | Option<[**Vec<String>**](String.md)> | Author criteria in the format: name,role. Multiple author criteria are supported. |  |

### Return type

[**models::PageBookDto**](PageBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

