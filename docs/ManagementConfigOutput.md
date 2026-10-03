# ManagementConfigOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backends** | [**Array&lt;ManagedBackend&gt;**](ManagedBackend.md) |  | [optional] [default to undefined]
**budget_allow_unpriced** | **boolean** |  | [optional] [default to false]
**catalog_models** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**keys** | [**Array&lt;ManagedKey&gt;**](ManagedKey.md) |  | [optional] [default to undefined]
**outbound_proxy** | **string** |  | [optional] [default to undefined]
**proxies** | [**Array&lt;ManagedProxy&gt;**](ManagedProxy.md) |  | [optional] [default to undefined]
**routing_default_optimize** | **string** |  | [optional] [default to RoutingDefaultOptimizeEnum_Balanced]
**routing_profiles** | [**{ [key: string]: ManagedRoutingProfile; }**](ManagedRoutingProfile.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ManagementConfigOutput } from 'mm-gateway-ts';

const instance: ManagementConfigOutput = {
    backends,
    budget_allow_unpriced,
    catalog_models,
    keys,
    outbound_proxy,
    proxies,
    routing_default_optimize,
    routing_profiles,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
