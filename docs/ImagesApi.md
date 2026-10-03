# ImagesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createImage**](#createimage) | **POST** /v1/images | Create an image task|
|[**estimateImage**](#estimateimage) | **POST** /v1/images/estimate | Estimate an image request|
|[**getImage**](#getimage) | **GET** /v1/images/{image_id} | Retrieve an image task|

# **createImage**
> ImageTaskResponse createImage(imageRequest)


### Example

```typescript
import {
    ImagesApi,
    Configuration,
    ImageRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ImagesApi(configuration);

let imageRequest: ImageRequest; //
let idempotencyKey: string; //Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional) (default to undefined)

const { status, data } = await apiInstance.createImage(
    imageRequest,
    idempotencyKey
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **imageRequest** | **ImageRequest**|  | |
| **idempotencyKey** | [**string**] | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | (optional) defaults to undefined|


### Return type

**ImageTaskResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | The image task was accepted. |  * ETag - Version identifier for conditional polling. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**409** | Idempotency key conflicts with an earlier request. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **estimateImage**
> EstimateResponse estimateImage(imageRequest)


### Example

```typescript
import {
    ImagesApi,
    Configuration,
    ImageRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ImagesApi(configuration);

let imageRequest: ImageRequest; //

const { status, data } = await apiInstance.estimateImage(
    imageRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **imageRequest** | **ImageRequest**|  | |


### Return type

**EstimateResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | How auto mode would route the request, and its estimated cost. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getImage**
> ImageTaskResponse getImage()


### Example

```typescript
import {
    ImagesApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ImagesApi(configuration);

let imageId: string; //Opaque image task id. (default to undefined)
let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.getImage(
    imageId,
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **imageId** | [**string**] | Opaque image task id. | defaults to undefined|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**ImageTaskResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The latest image task state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
|**304** | The task representation has not changed. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Unknown image task id. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

