# \ReleasesApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_releases**](ReleasesApi.md#get_releases) | **GET** /api/v1/releases | List releases



## get_releases

> Vec<models::ReleaseDto> get_releases()
List releases

Required role: **ADMIN**

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::ReleaseDto>**](ReleaseDto.md)

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

