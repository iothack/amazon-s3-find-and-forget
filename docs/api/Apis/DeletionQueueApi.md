# DeletionQueueApi

All URIs are relative to *https://your-apigw-id.execute-api.region.amazonaws.com/Prod*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddToDeletionQueue**](DeletionQueueApi.md#addtodeletionqueue) | **PATCH** /v1/queue | Adds an item to the deletion queue
[**DeleteMatches**](DeletionQueueApi.md#deletematches) | **DELETE** /v1/queue/matches | Removes an item from the deletion queue
[**ListDeletionQueueMatches**](DeletionQueueApi.md#listdeletionqueuematches) | **GET** /v1/queue | Lists deletion queue items
[**StartDeletionJob**](DeletionQueueApi.md#startdeletionjob) | **DELETE** /v1/queue | Starts a job for the items in the deletion queue


<a name="addtodeletionqueue"></a>
## **AddToDeletionQueue**

Adds an item to the deletion queue

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateDeletionQueueItem** | [**CreateDeletionQueueItem**](../Models/CreateDeletionQueueItem.md)| Request body containing details of the Match to add to the Deletion Queue |

### Return type

[**DeletionQueueItem**](../Models/DeletionQueueItem.md)

### Authorization

[CognitoAuthorizer](../README.md#CognitoAuthorizer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

<a name="deletematches"></a>
## **DeleteMatches**

Removes an item from the deletion queue

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ListOfMatchDeletions** | [**ListOfMatchDeletions**](../Models/ListOfMatchDeletions.md)|  |

### Return type

null (empty response body)

### Authorization

[CognitoAuthorizer](../README.md#CognitoAuthorizer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

<a name="listdeletionqueuematches"></a>
## **ListDeletionQueueMatches**

Lists deletion queue items

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **StartAt** | **String**| Start at watermark query string parameter | [optional] [default to 0]
 **PageSize** | **Integer**| Page size query string parameter. Min: 1. Max: 1000 | [optional] [default to null]

### Return type

[**DeletionQueue**](../Models/DeletionQueue.md)

### Authorization

[CognitoAuthorizer](../README.md#CognitoAuthorizer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

<a name="startdeletionjob"></a>
## **StartDeletionJob**

Starts a job for the items in the deletion queue

### Parameters
This endpoint does not need any parameters.

### Return type

[**Job**](../Models/Job.md)

### Authorization

[CognitoAuthorizer](../README.md#CognitoAuthorizer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

