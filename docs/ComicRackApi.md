# \ComicRackApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**match_comic_rack_list**](ComicRackApi.md#match_comic_rack_list) | **POST** /api/v1/readlists/match/comicrack | Match ComicRack list



## match_comic_rack_list

> models::ReadListRequestMatchDto match_comic_rack_list(add_user_uploaded_book_thumbnail_request)
Match ComicRack list

Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**add_user_uploaded_book_thumbnail_request** | Option<[**AddUserUploadedBookThumbnailRequest**](AddUserUploadedBookThumbnailRequest.md)> |  |  |

### Return type

[**models::ReadListRequestMatchDto**](ReadListRequestMatchDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

