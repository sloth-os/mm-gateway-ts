# MetaApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getHealth**](#gethealth) | **GET** /health | Health|
|[**getMetrics**](#getmetrics) | **GET** /metrics | Metrics|
|[**listModelLimits**](#listmodellimits) | **GET** /v1/models/limits | List Model Limits|
|[**listModels**](#listmodels) | **GET** /v1/models | List Models|

# **getHealth**
> HealthResponse getHealth()


### Example

```typescript
import {
    MetaApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new MetaApi(configuration);

const { status, data } = await apiInstance.getHealth();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**HealthResponse**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Gateway is healthy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getMetrics**
> string getMetrics()


### Example

```typescript
import {
    MetaApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new MetaApi(configuration);

const { status, data } = await apiInstance.getMetrics();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Prometheus exposition |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listModelLimits**
> ModelLimitsListResponse listModelLimits()

List usable models with their documented input/output limits.  Use this to pick a model and craft a prompt that fits: each entry\'s ``limits`` carries the input modalities accepted, the max prompt length, the max output count, supported sizes/durations, and per-role support flags (image-to-image, first/last frame, reference audio, lyrics, ...). The same catalogue drives auto-routing when a request omits ``model``.

### Example

```typescript
import {
    MetaApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new MetaApi(configuration);

let modality: 'image' | 'video' | 'music' | 'audio'; //Filter models by output modality. (optional) (default to undefined)
let authorization: string; //Bearer token: \"Bearer <api-key>\". (optional) (default to undefined)
let xRequestId: string; //Client-supplied request id (echoed back). (optional) (default to undefined)
let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.listModelLimits(
    modality,
    authorization,
    xRequestId,
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **modality** | [**&#39;image&#39; | &#39;video&#39; | &#39;music&#39; | &#39;audio&#39;**]**Array<&#39;image&#39; &#124; &#39;video&#39; &#124; &#39;music&#39; &#124; &#39;audio&#39;>** | Filter models by output modality. | (optional) defaults to undefined|
| **authorization** | [**string**] | Bearer token: \&quot;Bearer &lt;api-key&gt;\&quot;. | (optional) defaults to undefined|
| **xRequestId** | [**string**] | Client-supplied request id (echoed back). | (optional) defaults to undefined|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**ModelLimitsListResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Models available to the authenticated client with their input/output limits. |  * ETag - Version identifier for conditional polling. <br>  |
|**304** | The model catalogue has not changed. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key |  -  |
|**403** | Key not allowed to use any generation service |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listModels**
> ModelListResponse listModels()


### Example

```typescript
import {
    MetaApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new MetaApi(configuration);

let modality: 'image' | 'video' | 'music' | 'audio'; //Filter models by output modality. (optional) (default to undefined)
let authorization: string; //Bearer token: \"Bearer <api-key>\". (optional) (default to undefined)
let xRequestId: string; //Client-supplied request id (echoed back). (optional) (default to undefined)
let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.listModels(
    modality,
    authorization,
    xRequestId,
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **modality** | [**&#39;image&#39; | &#39;video&#39; | &#39;music&#39; | &#39;audio&#39;**]**Array<&#39;image&#39; &#124; &#39;video&#39; &#124; &#39;music&#39; &#124; &#39;audio&#39;>** | Filter models by output modality. | (optional) defaults to undefined|
| **authorization** | [**string**] | Bearer token: \&quot;Bearer &lt;api-key&gt;\&quot;. | (optional) defaults to undefined|
| **xRequestId** | [**string**] | Client-supplied request id (echoed back). | (optional) defaults to undefined|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**ModelListResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Models available to the authenticated client. |  * ETag - Version identifier for conditional retrieval. <br>  |
|**304** | The model catalogue has not changed. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key |  -  |
|**403** | Key not allowed to use any generation service |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

