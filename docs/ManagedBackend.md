# ManagedBackend


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_key** | **string** |  | [optional] [default to undefined]
**base_url** | **string** |  | [optional] [default to undefined]
**credentials** | [**Array&lt;BackendCredential&gt;**](BackendCredential.md) |  | [optional] [default to undefined]
**enabled** | **boolean** |  | [optional] [default to true]
**extra** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**model_aliases** | **object** | Public alias to active upstream model id, scoped to this backend. | [optional] [default to undefined]
**models** | **{ [key: string]: Array&lt;string&gt;; }** | Active model allowlist by modality. Null uses provider defaults; {} disables all models. | [optional] [default to undefined]
**name** | **string** |  | [default to undefined]
**tags** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**type** | **string** |  | [default to undefined]

## Example

```typescript
import { ManagedBackend } from 'mm-gateway-ts';

const instance: ManagedBackend = {
    api_key,
    base_url,
    credentials,
    enabled,
    extra,
    model_aliases,
    models,
    name,
    tags,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
