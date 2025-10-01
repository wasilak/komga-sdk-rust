# \ReferentialMetadataApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_age_ratings**](ReferentialMetadataApi.md#get_age_ratings) | **GET** /api/v1/age-ratings | List age ratings
[**get_authors**](ReferentialMetadataApi.md#get_authors) | **GET** /api/v2/authors | List authors
[**get_authors_deprecated**](ReferentialMetadataApi.md#get_authors_deprecated) | **GET** /api/v1/authors | List authors
[**get_authors_names**](ReferentialMetadataApi.md#get_authors_names) | **GET** /api/v1/authors/names | List authors' names
[**get_authors_roles**](ReferentialMetadataApi.md#get_authors_roles) | **GET** /api/v1/authors/roles | List authors' roles
[**get_book_tags**](ReferentialMetadataApi.md#get_book_tags) | **GET** /api/v1/tags/book | List book tags
[**get_genres**](ReferentialMetadataApi.md#get_genres) | **GET** /api/v1/genres | List genres
[**get_languages**](ReferentialMetadataApi.md#get_languages) | **GET** /api/v1/languages | List languages
[**get_publishers**](ReferentialMetadataApi.md#get_publishers) | **GET** /api/v1/publishers | List publishers
[**get_series_release_dates**](ReferentialMetadataApi.md#get_series_release_dates) | **GET** /api/v1/series/release-dates | List series release dates
[**get_series_tags**](ReferentialMetadataApi.md#get_series_tags) | **GET** /api/v1/tags/series | List series tags
[**get_sharing_labels**](ReferentialMetadataApi.md#get_sharing_labels) | **GET** /api/v1/sharing-labels | List sharing labels
[**get_tags**](ReferentialMetadataApi.md#get_tags) | **GET** /api/v1/tags | List tags



## get_age_ratings

> Vec<String> get_age_ratings(library_id, collection_id)
List age ratings

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_authors

> models::PageAuthorDto get_authors(search, role, library_id, collection_id, series_id, readlist_id, unpaged, page, size)
List authors

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |
**role** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |
**series_id** | Option<**String**> |  |  |
**readlist_id** | Option<**String**> |  |  |
**unpaged** | Option<**bool**> |  |  |
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |

### Return type

[**models::PageAuthorDto**](PageAuthorDto.md)

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


## get_authors_names

> Vec<String> get_authors_names(search)
List authors' names

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | Option<**String**> |  |  |[default to ]

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_authors_roles

> Vec<String> get_authors_roles()
List authors' roles

### Parameters

This endpoint does not need any parameter.

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_tags

> Vec<String> get_book_tags(series_id, readlist_id, library_id)
List book tags

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | Option<**String**> |  |  |
**readlist_id** | Option<**String**> |  |  |
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_genres

> Vec<String> get_genres(library_id, collection_id)
List genres

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_languages

> Vec<String> get_languages(library_id, collection_id)
List languages

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_publishers

> Vec<String> get_publishers(library_id, collection_id)
List publishers

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_release_dates

> Vec<String> get_series_release_dates(library_id, collection_id)
List series release dates

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_series_tags

> Vec<String> get_series_tags(library_id, collection_id)
List series tags

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<**String**> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sharing_labels

> Vec<String> get_sharing_labels(library_id, collection_id)
List sharing labels

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tags

> Vec<String> get_tags(library_id, collection_id)
List tags

Can be filtered by various criteria

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**library_id** | Option<[**Vec<String>**](String.md)> |  |  |
**collection_id** | Option<**String**> |  |  |

### Return type

**Vec<String>**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

