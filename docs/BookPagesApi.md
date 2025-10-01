# \BookPagesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_book_page_by_number**](BookPagesApi.md#get_book_page_by_number) | **GET** /api/v1/books/{bookId}/pages/{pageNumber} | Get book page image
[**get_book_page_raw_by_number**](BookPagesApi.md#get_book_page_raw_by_number) | **GET** /api/v1/books/{bookId}/pages/{pageNumber}/raw | Get raw book page
[**get_book_page_thumbnail_by_number**](BookPagesApi.md#get_book_page_thumbnail_by_number) | **GET** /api/v1/books/{bookId}/pages/{pageNumber}/thumbnail | Get book page thumbnail
[**get_book_pages**](BookPagesApi.md#get_book_pages) | **GET** /api/v1/books/{bookId}/pages | List book pages



## get_book_page_by_number

> std::path::PathBuf get_book_page_by_number(book_id, page_number, convert, zero_based, accept, content_negotiation)
Get book page image

Required role: **PAGE_STREAMING**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**page_number** | **i32** |  | [required] |
**convert** | Option<**String**> | Convert the image to the provided format. |  |
**zero_based** | Option<**bool**> | If set to true, pages will start at index 0. If set to false, pages will start at index 1. |  |[default to false]
**accept** | Option<[**Vec<models::MediaType>**](models::MediaType.md)> | Some very limited server driven content negotiation is handled. If a book is a PDF book, and the Accept header contains 'application/pdf' as a more specific type than other 'image/' types, a raw PDF page will be returned. |  |
**content_negotiation** | Option<**bool**> |  |  |[default to true]

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, image/*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_page_raw_by_number

> String get_book_page_raw_by_number(book_id, page_number)
Get raw book page

Returns the book page in raw format, without content negotiation.  Required role: **PAGE_STREAMING**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**page_number** | **i32** |  | [required] |

### Return type

**String**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_page_thumbnail_by_number

> std::path::PathBuf get_book_page_thumbnail_by_number(book_id, page_number)
Get book page thumbnail

The image is resized to 300px on the largest dimension.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**page_number** | **i32** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_pages

> Vec<models::PageDto> get_book_pages(book_id)
List book pages

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**Vec<models::PageDto>**](PageDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

