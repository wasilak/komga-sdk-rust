# \FileSystemApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_directory_listing**](FileSystemApi.md#get_directory_listing) | **POST** /api/v1/filesystem | Directory listing



## get_directory_listing

> models::DirectoryListingDto get_directory_listing(directory_request_dto)
Directory listing

List folders and files from the host server's file system. If no request body is passed then the root directories are returned.  Required role: **ADMIN**

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**directory_request_dto** | Option<[**DirectoryRequestDto**](DirectoryRequestDto.md)> |  |  |

### Return type

[**models::DirectoryListingDto**](DirectoryListingDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

