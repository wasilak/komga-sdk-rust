# \AnnouncementsApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_announcements**](AnnouncementsApi.md#get_announcements) | **GET** /api/v1/announcements | Retrieve announcements
[**mark_announcements_read**](AnnouncementsApi.md#mark_announcements_read) | **PUT** /api/v1/announcements | Mark announcements as read



## get_announcements

> models::JsonFeedDto get_announcements()
Retrieve announcements

Required role: **ADMIN**

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::JsonFeedDto**](JsonFeedDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_announcements_read

> mark_announcements_read(request_body)
Mark announcements as read

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**Vec<String>**](String.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

