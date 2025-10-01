# \TasksApi

All URIs are relative to *https://demo.komga.org*

Method | HTTP request | Description
------------- | ------------- | -------------
[**empty_task_queue**](TasksApi.md#empty_task_queue) | **DELETE** /api/v1/tasks | Clear task queue



## empty_task_queue

> i32 empty_task_queue()
Clear task queue

Cancel all tasks queued  Required role: **ADMIN**

### Parameters

This endpoint does not need any parameter.

### Return type

**i32**

### Authorization

[apiKey](../README.md#apiKey), [basicAuth](../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

