# \FontsApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_font_family_as_css**](FontsApi.md#get_font_family_as_css) | **GET** /api/v1/fonts/resource/{fontFamily}/css | Download CSS file
[**get_font_file**](FontsApi.md#get_font_file) | **GET** /api/v1/fonts/resource/{fontFamily}/{fontFile} | Download font file
[**get_fonts**](FontsApi.md#get_fonts) | **GET** /api/v1/fonts/families | List font families



## get_font_family_as_css

> std::path::PathBuf get_font_family_as_css(font_family)
Download CSS file

Download a CSS file with the @font-face block for the font family. This is used by the Epub Reader to change fonts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**font_family** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/css, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_font_file

> std::path::PathBuf get_font_file(font_family, font_file)
Download font file

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**font_family** | **String** |  | [required] |
**font_file** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_fonts

> Vec<String> get_fonts()
List font families

List all available font families.

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

