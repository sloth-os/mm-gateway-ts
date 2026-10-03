# AudioApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAudio**](#createaudio) | **POST** /v1/audio | Create a speech task|
|[**createVoice**](#createvoice) | **POST** /v1/voices | Clone a reusable voice|
|[**estimateAudio**](#estimateaudio) | **POST** /v1/audio/estimate | Estimate a speech request|
|[**estimateVoice**](#estimatevoice) | **POST** /v1/voices/estimate | Estimate voice cloning|
|[**getAudio**](#getaudio) | **GET** /v1/audio/{audio_id} | Retrieve a speech task|
|[**getVoice**](#getvoice) | **GET** /v1/voices/{voice_id} | Retrieve a voice or clone task|
|[**listVoices**](#listvoices) | **GET** /v1/voices | List usable voice presets and owned clones|

# **createAudio**
> AudioTaskResponse createAudio(audioRequest)


### Example

```typescript
import {
    AudioApi,
    Configuration,
    AudioRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let audioRequest: AudioRequest; //
let idempotencyKey: string; //Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional) (default to undefined)

const { status, data } = await apiInstance.createAudio(
    audioRequest,
    idempotencyKey
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **audioRequest** | **AudioRequest**|  | |
| **idempotencyKey** | [**string**] | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | (optional) defaults to undefined|


### Return type

**AudioTaskResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | Speech synthesis accepted. |  * ETag - Version identifier for conditional retrieval. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
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

# **createVoice**
> VoiceResponse createVoice(voiceCloneRequest)


### Example

```typescript
import {
    AudioApi,
    Configuration,
    VoiceCloneRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let voiceCloneRequest: VoiceCloneRequest; //
let idempotencyKey: string; //Client-generated key used to safely retry this create request. Reuse with a different body returns 409. (optional) (default to undefined)

const { status, data } = await apiInstance.createVoice(
    voiceCloneRequest,
    idempotencyKey
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **voiceCloneRequest** | **VoiceCloneRequest**|  | |
| **idempotencyKey** | [**string**] | Client-generated key used to safely retry this create request. Reuse with a different body returns 409. | (optional) defaults to undefined|


### Return type

**VoiceResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | Voice cloning accepted. |  * ETag - Version identifier for conditional polling. <br>  * Idempotency-Replayed - true when the response replays an earlier create request. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Location - Canonical URL of the created task resource. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
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

# **estimateAudio**
> EstimateResponse estimateAudio(audioRequest)


### Example

```typescript
import {
    AudioApi,
    Configuration,
    AudioRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let audioRequest: AudioRequest; //

const { status, data } = await apiInstance.estimateAudio(
    audioRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **audioRequest** | **AudioRequest**|  | |


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

# **estimateVoice**
> EstimateResponse estimateVoice(voiceCloneRequest)


### Example

```typescript
import {
    AudioApi,
    Configuration,
    VoiceCloneRequest
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let voiceCloneRequest: VoiceCloneRequest; //

const { status, data } = await apiInstance.estimateVoice(
    voiceCloneRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **voiceCloneRequest** | **VoiceCloneRequest**|  | |


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

# **getAudio**
> AudioTaskResponse getAudio()


### Example

```typescript
import {
    AudioApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let audioId: string; //Opaque speech task id. (default to undefined)
let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.getAudio(
    audioId,
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **audioId** | [**string**] | Opaque speech task id. | defaults to undefined|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**AudioTaskResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Current speech task state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
|**304** | Unchanged speech task. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getVoice**
> VoiceResponse getVoice()


### Example

```typescript
import {
    AudioApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let voiceId: string; //Gateway voice id. (default to undefined)
let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.getVoice(
    voiceId,
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **voiceId** | [**string**] | Gateway voice id. | defaults to undefined|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**VoiceResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Current voice state. |  * ETag - Version identifier for conditional polling. <br>  * Link - Canonical task URL with rel&#x3D;\&quot;self\&quot;. <br>  * Retry-After - Suggested number of seconds before polling again. <br>  |
|**304** | Unchanged voice. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listVoices**
> VoiceListResponse listVoices()


### Example

```typescript
import {
    AudioApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new AudioApi(configuration);

let ifNoneMatch: string; //Previously returned ETag; unchanged resources return 304. (optional) (default to undefined)

const { status, data } = await apiInstance.listVoices(
    ifNoneMatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ifNoneMatch** | [**string**] | Previously returned ETag; unchanged resources return 304. | (optional) defaults to undefined|


### Return type

**VoiceListResponse**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Voices available to this key. |  * ETag - Version identifier for conditional polling. <br>  |
|**304** | Unchanged voice list. |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key (unauthorized). |  -  |
|**403** | Key not allowed to perform the request (forbidden). |  -  |
|**404** | Model or task not found. |  -  |
|**422** | Validation Error |  -  |
|**502** | Generation service returned an error. |  -  |
|**503** | No usable generation service is configured. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

