# \DuplicatePagesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_or_update_known_page_hash**](DuplicatePagesApi.md#create_or_update_known_page_hash) | **PUT** /api/v1/page-hashes | Mark duplicate page as known
[**delete_duplicate_pages_by_page_hash**](DuplicatePagesApi.md#delete_duplicate_pages_by_page_hash) | **POST** /api/v1/page-hashes/{pageHash}/delete-all | Delete all duplicate pages by hash
[**delete_single_match_by_page_hash**](DuplicatePagesApi.md#delete_single_match_by_page_hash) | **POST** /api/v1/page-hashes/{pageHash}/delete-match | Delete specific duplicate page
[**get_known_page_hash_thumbnail**](DuplicatePagesApi.md#get_known_page_hash_thumbnail) | **GET** /api/v1/page-hashes/{pageHash}/thumbnail | Get known duplicate image thumbnail
[**get_known_page_hashes**](DuplicatePagesApi.md#get_known_page_hashes) | **GET** /api/v1/page-hashes | List known duplicates
[**get_page_hash_matches**](DuplicatePagesApi.md#get_page_hash_matches) | **GET** /api/v1/page-hashes/{pageHash} | List duplicate matches
[**get_unknown_page_hash_thumbnail**](DuplicatePagesApi.md#get_unknown_page_hash_thumbnail) | **GET** /api/v1/page-hashes/unknown/{pageHash}/thumbnail | Get unknown duplicate image thumbnail
[**get_unknown_page_hashes**](DuplicatePagesApi.md#get_unknown_page_hashes) | **GET** /api/v1/page-hashes/unknown | List unknown duplicates



## create_or_update_known_page_hash

> create_or_update_known_page_hash(page_hash_creation_dto)
Mark duplicate page as known

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash_creation_dto** | [**PageHashCreationDto**](PageHashCreationDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_duplicate_pages_by_page_hash

> delete_duplicate_pages_by_page_hash(page_hash)
Delete all duplicate pages by hash

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_single_match_by_page_hash

> delete_single_match_by_page_hash(page_hash, page_hash_match_dto)
Delete specific duplicate page

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash** | **String** |  | [required] |
**page_hash_match_dto** | [**PageHashMatchDto**](PageHashMatchDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_known_page_hash_thumbnail

> std::path::PathBuf get_known_page_hash_thumbnail(page_hash)
Get known duplicate image thumbnail

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_known_page_hashes

> models::PagePageHashKnownDto get_known_page_hashes(action, page, size, sort)
List known duplicates

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**action** | Option<[**Vec<String>**](String.md)> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PagePageHashKnownDto**](PagePageHashKnownDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_page_hash_matches

> models::PagePageHashMatchDto get_page_hash_matches(page_hash, page, size, sort)
List duplicate matches

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash** | **String** |  | [required] |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PagePageHashMatchDto**](PagePageHashMatchDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_unknown_page_hash_thumbnail

> std::path::PathBuf get_unknown_page_hash_thumbnail(page_hash, resize)
Get unknown duplicate image thumbnail

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_hash** | **String** |  | [required] |
**resize** | Option<**i32**> |  |  |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json, image/jpeg

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_unknown_page_hashes

> models::PagePageHashUnknownDto get_unknown_page_hashes(page, size, sort)
List unknown duplicates

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PagePageHashUnknownDto**](PagePageHashUnknownDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

