# ManagementStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backend_types** | **Array&lt;string&gt;** |  | [default to undefined]
**backends** | [**Array&lt;BackendRuntime&gt;**](BackendRuntime.md) |  | [default to undefined]
**enabled_keys_count** | **number** |  | [default to undefined]
**keys_count** | **number** |  | [default to undefined]
**metrics_enabled** | **boolean** |  | [default to undefined]
**persistent** | **boolean** |  | [default to undefined]
**proxies** | [**Array&lt;ProxyRuntime&gt;**](ProxyRuntime.md) |  | [default to undefined]
**revision** | **string** |  | [default to undefined]
**status** | **string** |  | [optional] [default to StatusEnum_Ok]
**tasks_by_status** | **{ [key: string]: number; }** |  | [default to undefined]
**uptime_seconds** | **number** |  | [default to undefined]
**version** | **string** |  | [default to undefined]

## Example

```typescript
import { ManagementStatus } from 'mm-gateway-ts';

const instance: ManagementStatus = {
    backend_types,
    backends,
    enabled_keys_count,
    keys_count,
    metrics_enabled,
    persistent,
    proxies,
    revision,
    status,
    tasks_by_status,
    uptime_seconds,
    version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
