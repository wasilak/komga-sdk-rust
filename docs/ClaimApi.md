# \ClaimApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**claim_server**](ClaimApi.md#claim_server) | **POST** /api/v1/claim | Claim server
[**get_claim_status**](ClaimApi.md#get_claim_status) | **GET** /api/v1/claim | Retrieve claim status



## claim_server

> models::UserDto claim_server(x_komga_email, x_komga_password)
Claim server

Creates an admin user with the provided credentials.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_komga_email** | **String** |  | [required] |
**x_komga_password** | **String** |  | [required] |

### Return type

[**models::UserDto**](UserDto.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_claim_status

> models::ClaimStatus get_claim_status()
Retrieve claim status

Check whether this server has already been claimed.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ClaimStatus**](ClaimStatus.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

