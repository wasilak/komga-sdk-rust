# \MihonApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_mihon_read_progress_by_read_list_id**](MihonApi.md#get_mihon_read_progress_by_read_list_id) | **GET** /api/v1/readlists/{id}/read-progress/tachiyomi | Get readlist read progress (Mihon)
[**get_mihon_read_progress_by_series_id**](MihonApi.md#get_mihon_read_progress_by_series_id) | **GET** /api/v2/series/{seriesId}/read-progress/tachiyomi | Get series read progress (Mihon)
[**update_mihon_read_progress_by_read_list_id**](MihonApi.md#update_mihon_read_progress_by_read_list_id) | **PUT** /api/v1/readlists/{id}/read-progress/tachiyomi | Update readlist read progress (Mihon)
[**update_mihon_read_progress_by_series_id**](MihonApi.md#update_mihon_read_progress_by_series_id) | **PUT** /api/v2/series/{seriesId}/read-progress/tachiyomi | Update series read progress (Mihon)



## get_mihon_read_progress_by_read_list_id

> models::TachiyomiReadProgressDto get_mihon_read_progress_by_read_list_id(id)
Get readlist read progress (Mihon)

Mihon specific, due to how read progress is handled in Mihon.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::TachiyomiReadProgressDto**](TachiyomiReadProgressDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_mihon_read_progress_by_series_id

> models::TachiyomiReadProgressV2Dto get_mihon_read_progress_by_series_id(series_id)
Get series read progress (Mihon)

Mihon specific, due to how read progress is handled in Mihon.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |

### Return type

[**models::TachiyomiReadProgressV2Dto**](TachiyomiReadProgressV2Dto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_mihon_read_progress_by_read_list_id

> update_mihon_read_progress_by_read_list_id(id, tachiyomi_read_progress_update_dto)
Update readlist read progress (Mihon)

Mihon specific, due to how read progress is handled in Mihon.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**tachiyomi_read_progress_update_dto** | [**TachiyomiReadProgressUpdateDto**](TachiyomiReadProgressUpdateDto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_mihon_read_progress_by_series_id

> update_mihon_read_progress_by_series_id(series_id, tachiyomi_read_progress_update_v2_dto)
Update series read progress (Mihon)

Mihon specific, due to how read progress is handled in Mihon.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**series_id** | **String** |  | [required] |
**tachiyomi_read_progress_update_v2_dto** | [**TachiyomiReadProgressUpdateV2Dto**](TachiyomiReadProgressUpdateV2Dto.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

