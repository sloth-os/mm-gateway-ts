# PluginEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | **boolean** |  | [optional] [default to false]
**calls** | **number** |  | [optional] [default to 0]
**error** | **string** |  | [optional] [default to undefined]
**failures** | **number** |  | [optional] [default to 0]
**generation** | **string** |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**installed** | **boolean** |  | [optional] [default to false]
**loaded_at** | **number** |  | [optional] [default to undefined]
**manifest** | [**PluginManifest**](PluginManifest.md) |  | [optional] [default to undefined]
**_options** | [**PluginOptions**](PluginOptions.md) |  | [optional] [default to undefined]
**source** | [**PluginSource**](PluginSource.md) |  | [default to undefined]

## Example

```typescript
import { PluginEntry } from 'mm-gateway-ts';

const instance: PluginEntry = {
    active,
    calls,
    error,
    failures,
    generation,
    id,
    installed,
    loaded_at,
    manifest,
    _options,
    source,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
