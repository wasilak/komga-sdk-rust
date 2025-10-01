# \BookPosterApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_uploaded_book_thumbnail**](BookPosterApi.md#add_user_uploaded_book_thumbnail) | **POST** /api/v1/books/{bookId}/thumbnails | Add book poster
[**books_regenerate_thumbnails**](BookPosterApi.md#books_regenerate_thumbnails) | **PUT** /api/v1/books/thumbnails | Regenerate books posters
[**delete_user_uploaded_book_thumbnail**](BookPosterApi.md#delete_user_uploaded_book_thumbnail) | **DELETE** /api/v1/books/{bookId}/thumbnails/{thumbnailId} | Delete book poster
[**get_book_thumbnail**](BookPosterApi.md#get_book_thumbnail) | **GET** /api/v1/books/{bookId}/thumbnail | Get book's poster image
[**get_book_thumbnail_by_id**](BookPosterApi.md#get_book_thumbnail_by_id) | **GET** /api/v1/books/{bookId}/thumbnails/{thumbnailId} | Get book poster image
[**get_book_thumbnails**](BookPosterApi.md#get_book_thumbnails) | **GET** /api/v1/books/{bookId}/thumbnails | List book posters
[**mark_book_thumbnail_selected**](BookPosterApi.md#mark_book_thumbnail_selected) | **PUT** /api/v1/books/{bookId}/thumbnails/{thumbnailId}/selected | Mark book poster as selected



## add_user_uploaded_book_thumbnail

> models::ThumbnailBookDto add_user_uploaded_book_thumbnail(book_id, file, selected)
Add book poster

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**file** | **std::path::PathBuf** |  | [required] |
**selected** | Option<**bool**> |  |  |

### Return type

[**models::ThumbnailBookDto**](ThumbnailBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## books_regenerate_thumbnails

> books_regenerate_thumbnails(for_bigger_result_only)
Regenerate books posters

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**for_bigger_result_only** | Option<**bool**> |  |  |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_user_uploaded_book_thumbnail

> delete_user_uploaded_book_thumbnail(book_id, thumbnail_id)
Delete book poster

Only uploaded posters can be deleted.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_thumbnail

> std::path::PathBuf get_book_thumbnail(book_id)
Get book's poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_thumbnail_by_id

> std::path::PathBuf get_book_thumbnail_by_id(book_id, thumbnail_id)
Get book poster image

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_thumbnails

> Vec<models::ThumbnailBookDto> get_book_thumbnails(book_id)
List book posters

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**Vec<models::ThumbnailBookDto>**](ThumbnailBookDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_book_thumbnail_selected

> mark_book_thumbnail_selected(book_id, thumbnail_id)
Mark book poster as selected

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**thumbnail_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

