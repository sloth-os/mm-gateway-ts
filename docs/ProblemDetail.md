# ProblemDetail

RFC 9457 problem details with stable gateway extensions.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | Stable machine-readable gateway error code. | [default to undefined]
**detail** | **string** | Human-readable detail for this occurrence. | [default to undefined]
**errors** | **Array&lt;{ [key: string]: any; }&gt;** | Field-level validation errors, when applicable. | [optional] [default to undefined]
**instance** | **string** | Previously returned ETag; unchanged resources return 304. | [optional] [default to undefined]
**request_id** | **string** | Previously returned ETag; unchanged resources return 304. | [optional] [default to undefined]
**status** | **number** | HTTP response status code. | [default to undefined]
**title** | **string** | Short, stable summary of the problem type. | [default to undefined]
**type** | **string** | URI identifying the problem type. | [default to undefined]

## Example

```typescript
import { ProblemDetail } from 'mm-gateway-ts';

const instance: ProblemDetail = {
    code,
    detail,
    errors,
    instance,
    request_id,
    status,
    title,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
