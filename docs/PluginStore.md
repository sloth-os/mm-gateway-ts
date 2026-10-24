# PluginStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**Array&lt;PluginEntry&gt;**](PluginEntry.md) |  | [default to undefined]
**directory** | **string** |  | [default to undefined]
**errors** | [**Array&lt;PluginDiscoveryError&gt;**](PluginDiscoveryError.md) |  | [default to undefined]
**persistent** | **boolean** |  | [default to undefined]
**revision** | **string** |  | [default to undefined]
**watching** | **boolean** |  | [default to undefined]

## Example

```typescript
import { PluginStore } from 'mm-gateway-ts';

const instance: PluginStore = {
    data,
    directory,
    errors,
    persistent,
    revision,
    watching,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
