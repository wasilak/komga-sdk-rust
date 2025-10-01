# \ImportApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyze_transient_book**](ImportApi.md#analyze_transient_book) | **POST** /api/v1/transient-books/{id}/analyze | Analyze transient book
[**get_page_by_transient_book_id**](ImportApi.md#get_page_by_transient_book_id) | **GET** /api/v1/transient-books/{id}/pages/{pageNumber} | Get transient book page
[**import_books**](ImportApi.md#import_books) | **POST** /api/v1/books/import | Import books
[**scan_transient_books**](ImportApi.md#scan_transient_books) | **POST** /api/v1/transient-books | Scan folder for transient books



## analyze_transient_book

> models::TransientBookDto analyze_transient_book(id)
Analyze transient book

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::TransientBookDto**](TransientBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_page_by_transient_book_id

> String get_page_by_transient_book_id(id, page_number)
Get transient book page

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**page_number** | **i32** |  | [required] |

### Return type

**String**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## import_books

> import_books(book_import_batch_dto)
Import books

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_import_batch_dto** | [**BookImportBatchDto**](BookImportBatchDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## scan_transient_books

> Vec<models::TransientBookDto> scan_transient_books(scan_request_dto)
Scan folder for transient books

Scan provided folder for transient books.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**scan_request_dto** | [**ScanRequestDto**](ScanRequestDto.md) |  | [required] |

### Return type

[**Vec<models::TransientBookDto>**](TransientBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

