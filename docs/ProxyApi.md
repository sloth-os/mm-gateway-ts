# ProxyApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**proxyRequestDelete**](#proxyrequestdelete) | **DELETE** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestGet**](#proxyrequestget) | **GET** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestHead**](#proxyrequesthead) | **HEAD** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestOptions**](#proxyrequestoptions) | **OPTIONS** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestPatch**](#proxyrequestpatch) | **PATCH** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestPost**](#proxyrequestpost) | **POST** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|
|[**proxyRequestPut**](#proxyrequestput) | **PUT** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy|

# **proxyRequestDelete**
> proxyRequestDelete()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestDelete(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestGet**
> proxyRequestGet()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestGet(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestHead**
> proxyRequestHead()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestHead(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestOptions**
> proxyRequestOptions()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestOptions(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestPatch**
> proxyRequestPatch()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestPatch(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestPost**
> proxyRequestPost()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestPost(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **proxyRequestPut**
> proxyRequestPut()

Forward an HTTP request through a domain-matched proxy to its upstream.  The path, query string, body, and most client headers are forwarded verbatim to ``{base_url}/{path}``; the configured account\'s credential is injected from the account\'s ``headers`` and the upstream response (including event streams) is streamed back. Retries across accounts on a rate-limit / timeout / 5xx.

### Example

```typescript
import {
    ProxyApi,
    Configuration
} from 'mm-gateway-ts';

const configuration = new Configuration();
const apiInstance = new ProxyApi(configuration);

let domain: string; //Configured proxy domain (the upstream host segment selecting the proxy). (default to undefined)
let path: string; //Path forwarded to the upstream root URL. (default to undefined)

const { status, data } = await apiInstance.proxyRequestPut(
    domain,
    path
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Configured proxy domain (the upstream host segment selecting the proxy). | defaults to undefined|
| **path** | [**string**] | Path forwarded to the upstream root URL. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/problem+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | The upstream response, streamed back verbatim (any media type). |  -  |
|**400** | Invalid request (invalid_request_error / unsupported_feature). |  -  |
|**401** | Missing or unknown API key. |  -  |
|**403** | Key not allowed to use this proxy. |  -  |
|**404** | No proxy configured for this domain. |  -  |
|**422** | Validation Error |  -  |
|**502** | Every upstream account failed. |  -  |
|**503** | The proxy has no configured account. |  -  |
|**504** | Generation service timed out. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

