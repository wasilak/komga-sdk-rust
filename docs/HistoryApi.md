# \HistoryApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_historical_events**](HistoryApi.md#get_historical_events) | **GET** /api/v1/history | List historical events



## get_historical_events

> models::PageHistoricalEventDto get_historical_events(page, size, sort)
List historical events

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Zero-based page index (0..N) |  |
**size** | Option<**i32**> | The size of the page to be returned |  |
**sort** | Option<[**Vec<String>**](String.md)> | Sorting criteria in the format: property(,asc|desc). Default sort order is ascending. Multiple sort criteria are supported. |  |

### Return type

[**models::PageHistoricalEventDto**](PageHistoricalEventDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

