# \WebPubManifestApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_book_epub_resource**](WebPubManifestApi.md#get_book_epub_resource) | **GET** /api/v1/books/{bookId}/resource/{resource} | Get Epub resource
[**get_book_positions**](WebPubManifestApi.md#get_book_positions) | **GET** /api/v1/books/{bookId}/positions | List book's positions
[**get_book_progression**](WebPubManifestApi.md#get_book_progression) | **GET** /api/v1/books/{bookId}/progression | Get book progression
[**get_book_web_pub_manifest**](WebPubManifestApi.md#get_book_web_pub_manifest) | **GET** /api/v1/books/{bookId}/manifest | Get book's WebPub manifest
[**get_book_web_pub_manifest_divina**](WebPubManifestApi.md#get_book_web_pub_manifest_divina) | **GET** /api/v1/books/{bookId}/manifest/divina | Get book's WebPub manifest (DiViNa)
[**get_book_web_pub_manifest_epub**](WebPubManifestApi.md#get_book_web_pub_manifest_epub) | **GET** /api/v1/books/{bookId}/manifest/epub | Get book's WebPub manifest (Epub)
[**get_book_web_pub_manifest_pdf**](WebPubManifestApi.md#get_book_web_pub_manifest_pdf) | **GET** /api/v1/books/{bookId}/manifest/pdf | Get book's WebPub manifest (PDF)
[**update_book_progression**](WebPubManifestApi.md#update_book_progression) | **PUT** /api/v1/books/{bookId}/progression | Mark book progression



## get_book_epub_resource

> String get_book_epub_resource(book_id, resource)
Get Epub resource

Return a resource from within an Epub book.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**resource** | **String** |  | [required] |

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: */*, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_positions

> models::R2Positions get_book_positions(book_id)
List book's positions

The Positions API is a proposed standard for OPDS 2 and Readium. It is used by the Epub Reader.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::R2Positions**](R2Positions.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/vnd.readium.position-list+json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_progression

> models::R2Progression get_book_progression(book_id)
Get book progression

The Progression API is a proposed standard for OPDS 2 and Readium. It is used by the Epub Reader.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::R2Progression**](R2Progression.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/vnd.readium.progression+json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_web_pub_manifest

> models::WpPublicationDto get_book_web_pub_manifest(book_id)
Get book's WebPub manifest

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::WpPublicationDto**](WPPublicationDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/divina+json, application/json, application/webpub+json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_web_pub_manifest_divina

> models::WpPublicationDto get_book_web_pub_manifest_divina(book_id)
Get book's WebPub manifest (DiViNa)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::WpPublicationDto**](WPPublicationDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/divina+json, application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_web_pub_manifest_epub

> models::WpPublicationDto get_book_web_pub_manifest_epub(book_id)
Get book's WebPub manifest (Epub)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::WpPublicationDto**](WPPublicationDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/webpub+json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_book_web_pub_manifest_pdf

> models::WpPublicationDto get_book_web_pub_manifest_pdf(book_id)
Get book's WebPub manifest (PDF)

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |

### Return type

[**models::WpPublicationDto**](WPPublicationDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/webpub+json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_book_progression

> update_book_progression(book_id, r2_progression)
Mark book progression

The Progression API is a proposed standard for OPDS 2 and Readium. It is used by the Epub Reader.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**book_id** | **String** |  | [required] |
**r2_progression** | [**R2Progression**](R2Progression.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

