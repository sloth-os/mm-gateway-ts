# PluginOptions


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**enabled** | **boolean** |  | [optional] [default to true]
**failure_mode** | **string** |  | [optional] [default to FailureModeEnum_Closed]
**order** | **number** |  | [optional] [default to 0]
**timeout_ms** | **number** |  | [optional] [default to 1000]

## Example

```typescript
import { PluginOptions } from 'mm-gateway-ts';

const instance: PluginOptions = {
    config,
    enabled,
    failure_mode,
    order,
    timeout_ms,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
