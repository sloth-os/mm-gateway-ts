# UsageApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getUsage**](#getusage) | **GET** /v1/usage | Spend and budgets of the authenticated key|

# **getUsage**
> UsageResponse getUsage()


### Example

```typescript
import {
    UsageApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new UsageApi(configuration);

let scope: string; //Report only this budget scope. (optional) (default to undefined)

const { status, data } = await apiInstance.getUsage(
    scope
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **scope** | [**string**] | Report only this budget scope. | (optional) defaults to undefined|


### Return type

**UsageResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Spend, reservations and budgets for the current period. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

