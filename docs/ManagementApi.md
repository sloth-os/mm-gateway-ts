# ManagementApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteManagementBackend**](#deletemanagementbackend) | **DELETE** /v1/management/backends/{name} | Delete Backend|
|[**deleteManagementKey**](#deletemanagementkey) | **DELETE** /v1/management/keys/{key_id} | Delete Key|
|[**deleteManagementProxy**](#deletemanagementproxy) | **DELETE** /v1/management/proxies/{domain} | Delete Proxy|
|[**getManagementConfig**](#getmanagementconfig) | **GET** /v1/management/config | Get Config|
|[**getManagementMetrics**](#getmanagementmetrics) | **GET** /v1/management/metrics | Get Metrics|
|[**getManagementStatus**](#getmanagementstatus) | **GET** /v1/management/status | Get Status|
|[**listManagementTasks**](#listmanagementtasks) | **GET** /v1/management/tasks | List Tasks|
|[**listManagementUsage**](#listmanagementusage) | **GET** /v1/management/usage | List Usage|
|[**putManagementBackend**](#putmanagementbackend) | **PUT** /v1/management/backends/{name} | Put Backend|
|[**putManagementKey**](#putmanagementkey) | **PUT** /v1/management/keys/{key_id} | Put Key|
|[**putManagementProxy**](#putmanagementproxy) | **PUT** /v1/management/proxies/{domain} | Put Proxy|
|[**replaceManagementConfig**](#replacemanagementconfig) | **PUT** /v1/management/config | Replace Config|

# **deleteManagementBackend**
> ManagementConfigResponse deleteManagementBackend()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let name: string; // (default to undefined)
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.deleteManagementBackend(
    name,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteManagementKey**
> ManagementConfigResponse deleteManagementKey()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let keyId: string; // (default to undefined)
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.deleteManagementKey(
    keyId,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **keyId** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteManagementProxy**
> ManagementConfigResponse deleteManagementProxy()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let domain: string; // (default to undefined)
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.deleteManagementProxy(
    domain,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getManagementConfig**
> ManagementConfigResponse getManagementConfig()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

const { status, data } = await apiInstance.getManagementConfig();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Request validation failed or a task failed. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getManagementMetrics**
> ManagementMetrics getManagementMetrics()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

const { status, data } = await apiInstance.getManagementMetrics();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**ManagementMetrics**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Request validation failed or a task failed. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getManagementStatus**
> ManagementStatus getManagementStatus()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

const { status, data } = await apiInstance.getManagementStatus();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**ManagementStatus**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Request validation failed or a task failed. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listManagementTasks**
> ManagementTaskList listManagementTasks()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let modality: 'image' | 'video' | 'music' | 'audio' | 'voice'; // (optional) (default to undefined)
let status: 'pending' | 'running' | 'succeeded' | 'failed' | 'cancelled' | 'expired'; // (optional) (default to undefined)
let keyId: string; // (optional) (default to undefined)
let backend: string; // (optional) (default to undefined)
let offset: number; // (optional) (default to 0)
let limit: number; // (optional) (default to 50)

const { status, data } = await apiInstance.listManagementTasks(
    modality,
    status,
    keyId,
    backend,
    offset,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **modality** | [**&#39;image&#39; | &#39;video&#39; | &#39;music&#39; | &#39;audio&#39; | &#39;voice&#39;**]**Array<&#39;image&#39; &#124; &#39;video&#39; &#124; &#39;music&#39; &#124; &#39;audio&#39; &#124; &#39;voice&#39;>** |  | (optional) defaults to undefined|
| **status** | [**&#39;pending&#39; | &#39;running&#39; | &#39;succeeded&#39; | &#39;failed&#39; | &#39;cancelled&#39; | &#39;expired&#39;**]**Array<&#39;pending&#39; &#124; &#39;running&#39; &#124; &#39;succeeded&#39; &#124; &#39;failed&#39; &#124; &#39;cancelled&#39; &#124; &#39;expired&#39;>** |  | (optional) defaults to undefined|
| **keyId** | [**string**] |  | (optional) defaults to undefined|
| **backend** | [**string**] |  | (optional) defaults to undefined|
| **offset** | [**number**] |  | (optional) defaults to 0|
| **limit** | [**number**] |  | (optional) defaults to 50|


### Return type

**ManagementTaskList**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listManagementUsage**
> ManagementUsageList listManagementUsage()


### Example

```typescript
import {
    ManagementApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let keyId: string; // (optional) (default to undefined)

const { status, data } = await apiInstance.listManagementUsage(
    keyId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **keyId** | [**string**] |  | (optional) defaults to undefined|


### Return type

**ManagementUsageList**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **putManagementBackend**
> ManagementConfigResponse putManagementBackend(managedBackend)


### Example

```typescript
import {
    ManagementApi,
    Configuration,
    ManagedBackend
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let name: string; // (default to undefined)
let managedBackend: ManagedBackend; //
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.putManagementBackend(
    name,
    managedBackend,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **managedBackend** | **ManagedBackend**|  | |
| **name** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **putManagementKey**
> ManagementConfigResponse putManagementKey(managedKey)


### Example

```typescript
import {
    ManagementApi,
    Configuration,
    ManagedKey
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let keyId: string; // (default to undefined)
let managedKey: ManagedKey; //
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.putManagementKey(
    keyId,
    managedKey,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **managedKey** | **ManagedKey**|  | |
| **keyId** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **putManagementProxy**
> ManagementConfigResponse putManagementProxy(managedProxy)


### Example

```typescript
import {
    ManagementApi,
    Configuration,
    ManagedProxy
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let domain: string; // (default to undefined)
let managedProxy: ManagedProxy; //
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.putManagementProxy(
    domain,
    managedProxy,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **managedProxy** | **ManagedProxy**|  | |
| **domain** | [**string**] |  | defaults to undefined|
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replaceManagementConfig**
> ManagementConfigResponse replaceManagementConfig(managementConfigInput)


### Example

```typescript
import {
    ManagementApi,
    Configuration,
    ManagementConfigInput
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ManagementApi(configuration);

let managementConfigInput: ManagementConfigInput; //
let ifMatch: string; //Current configuration revision (ETag). (optional) (default to undefined)

const { status, data } = await apiInstance.replaceManagementConfig(
    managementConfigInput,
    ifMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **managementConfigInput** | **ManagementConfigInput**|  | |
| **ifMatch** | [**string**] | Current configuration revision (ETag). | (optional) defaults to undefined|


### Return type

**ManagementConfigResponse**

### Authorization

[ManagementAuth](../README.md#ManagementAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Successful Response |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**404** | Model or task not found. |  -  |
|**412** | Configuration changed; reload before saving. |  -  |
|**422** | Validation Error |  -  |
|**428** | A current If-Match revision is required. |  -  |
|**503** | No usable generation service is configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

